## API Report File for "pnpm-sync-lib"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @beta (undocumented)
export interface IDependencyMeta {
    // (undocumented)
    injected?: boolean;
}

// @beta
export interface ILockfile {
    // (undocumented)
    importers: Record<string, ILockfileImporter>;
}

// @beta (undocumented)
export interface ILockfileImporter {
    // (undocumented)
    dependencies?: Record<string, IVersionSpecifier>;
    // (undocumented)
    dependenciesMeta?: Record<string, IDependencyMeta>;
    // (undocumented)
    devDependencies?: Record<string, IVersionSpecifier>;
    // (undocumented)
    optionalDependencies?: Record<string, IVersionSpecifier>;
}

// @beta (undocumented)
export interface IPnpmSyncCopyOptions {
    // (undocumented)
    ensureFolder: (folderPath: string) => Promise<void>;
    // (undocumented)
    forEachAsyncWithConcurrency: <TItem>(iterable: Iterable<TItem>, callback: (item: TItem) => Promise<void>, options: {
        concurrency: number;
    }) => Promise<void>;
    // (undocumented)
    getPackageIncludedFiles: (packagePath: string) => Promise<string[]>;
    // (undocumented)
    pnpmSyncJsonPath?: string;
}

// @beta (undocumented)
export interface IPnpmSyncPrepareOptions {
    // (undocumented)
    lockfilePath: string;
    // (undocumented)
    readWantedLockfile: (lockfilePath: string, options: {
        ignoreIncompatible: boolean;
    }) => Promise<ILockfile | null>;
    // (undocumented)
    storePath: string;
}

// @beta (undocumented)
export type IVersionSpecifier = string | {
    version: string;
};

// @beta
export function pnpmSyncCopyAsync({ pnpmSyncJsonPath, getPackageIncludedFiles, forEachAsyncWithConcurrency, ensureFolder, }: IPnpmSyncCopyOptions): Promise<void>;

// @beta
export function pnpmSyncPrepareAsync({ lockfilePath, storePath, readWantedLockfile, }: IPnpmSyncPrepareOptions): Promise<void>;

```
