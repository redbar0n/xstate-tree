## API Report File for "@koordinates/xstate-tree"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AnyEventObject } from 'xstate';
import type { AnyFunction } from 'xstate';
import { AnyStateMachine } from 'xstate';
import { BaseActionObject } from 'xstate';
import { ComponentPropsWithRef } from 'react';
import { ContextFrom } from 'xstate';
import { EventFrom } from 'xstate';
import { EventObject } from 'xstate';
import { History as History_2 } from 'history';
import type { InterpreterFrom } from 'xstate';
import { JSXElementConstructor } from 'react';
import { ParsedQuery } from 'query-string';
import { default as React_2 } from 'react';
import { ResolveTypegenMeta } from 'xstate';
import { ServiceMap } from 'xstate';
import type { StateFrom } from 'xstate';
import { StateMachine } from 'xstate';
import { TypegenDisabled } from 'xstate';
import * as Z from 'zod';

// @public (undocumented)
export type AnyActions = (send: any, selectors: any) => any;

// @public (undocumented)
export type AnyRoute = {
    matches: (url: string, search: string) => any;
    reverse: any;
    navigate: any;
    getEvent: any;
    event: string;
    url?: string;
    basePath: string;
    history: XstateTreeHistory;
    parent?: AnyRoute;
    paramsSchema?: Z.ZodObject<any>;
    querySchema?: Z.ZodObject<any>;
};

// @public (undocumented)
export type AnySelector = Selectors<any, any, any, any>;

// @public (undocumented)
export type AnyXstateTreeMachine = StateMachine<any, XstateTreeMachineStateSchema<AnyStateMachine, any, any>, any>;

// @public (undocumented)
export type ArgumentsForRoute<T> = T extends Route<infer TParams, infer TQuery, any, infer TMeta> ? RouteArguments<TParams, TQuery, TMeta> : never;

// @public
export function broadcast(event: GlobalEvents): void;

// @public
export function buildActions<TMachine extends AnyStateMachine, TActions, TSelectors, TSend = InterpreterFrom<TMachine>["send"]>(__machine: TMachine, __selectors: TSelectors, actions: (send: TSend, selectors: OutputFromSelector<TSelectors>) => TActions): (send: TSend, selectors: OutputFromSelector<TSelectors>) => TActions;

// @public
export function buildCreateRoute(history: XstateTreeHistory, basePath: string): {
    dynamicRoute: <TOpts extends Options<Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }>, Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }>, any>>(opts?: TOpts | undefined) => <TEvent extends string, TParamsSchema = Params<TOpts>, TQuerySchema = Query<TOpts>, TMeta = Meta<TOpts>, TParams = TParamsSchema extends Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }> ? Z.TypeOf<TParamsSchema> : undefined, TQuery = TQuerySchema extends Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }> ? Z.TypeOf<TQuerySchema> : undefined, TFullMeta = TMeta extends undefined ? SharedMeta : TMeta & SharedMeta>({ event, matches, reverse, }: {
        event: TEvent;
        matches: (url: string, query: ParsedQuery<string>) => false | RouteArguments<TParams, TQuery, TFullMeta>;
        reverse: RouteArgumentFunctions<string, TParams, TQuery, TFullMeta, RouteArguments<TParams, TQuery, TFullMeta>>;
    }) => Route<TParams, TQuery, TEvent, TFullMeta>;
    staticRoute: <TBaseRoute extends AnyRoute | undefined = undefined, TBaseParams = RouteParams<TBaseRoute>, TBaseMeta = RouteMeta<TBaseRoute>>(baseRoute?: TBaseRoute | undefined) => <TOpts_1 extends Options<Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }>, Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }>, any>, TEvent_1 extends string, TParamsSchema_1 = Params<TOpts_1>, TQuerySchema_1 = Query<TOpts_1>, TMeta_1 = Meta<TOpts_1>, TParams_1 = TParamsSchema_1 extends Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }> ? Z.TypeOf<TParamsSchema_1> : undefined, TQuery_1 = TQuerySchema_1 extends Z.ZodObject<any, "strip", Z.ZodTypeAny, {
        [x: string]: any;
    }, {
        [x: string]: any;
    }> ? Z.TypeOf<TQuerySchema_1> : undefined, TFullParams = TParams_1 extends undefined ? TBaseParams extends undefined ? undefined : TBaseParams : TParams_1 & (TBaseParams extends undefined ? {} : TBaseParams), TFullMeta_1 = TMeta_1 extends undefined ? TBaseMeta extends undefined ? SharedMeta : TBaseMeta & SharedMeta : TMeta_1 & (TBaseMeta extends undefined ? {} : TBaseMeta) & SharedMeta>(url: string, event: TEvent_1, opts?: TOpts_1 | undefined) => Route<TFullParams, TQuery_1, TEvent_1, TFullMeta_1>;
};

// @public
export function buildRootComponent(machine: AnyXstateTreeMachine, routing?: {
    routes: AnyRoute[];
    history: XstateTreeHistory<any>;
    basePath: string;
    getPathName?: () => string;
    getQueryString?: () => string;
}): {
    (): JSX.Element | null;
    rootMachine: AnyXstateTreeMachine;
};

// Warning: (ae-forgotten-export) The symbol "CanHandleEvent" needs to be exported by the entry point index.d.ts
// Warning: (ae-incompatible-release-tags) The symbol "buildSelectors" is marked as @public, but its signature references "MatchesFrom" which is marked as @internal
//
// @public
export function buildSelectors<TMachine extends AnyStateMachine, TSelectors, TContext = ContextFrom<TMachine>>(__machine: TMachine, selectors: (ctx: TContext, canHandleEvent: CanHandleEvent<TMachine>, inState: MatchesFrom<TMachine>, __currentState: never) => TSelectors): Selectors<TContext, EventFrom<TMachine>, TSelectors, MatchesFrom<TMachine>>;

// @public
export function buildTestRootComponent<TMachine extends AnyStateMachine, TSelectors extends AnySelector, TActions extends AnyActions, TContext = ContextFrom<TMachine>>(machine: StateMachine<TContext, XstateTreeMachineStateSchema<TMachine, TSelectors, TActions>, EventFrom<TMachine>>, logger: typeof console.log): {
    rootComponent: () => JSX.Element | null;
    addTransitionListener: (listener: () => void) => void;
    awaitTransition(): Promise<void>;
};

// Warning: (ae-incompatible-release-tags) The symbol "buildView" is marked as @public, but its signature references "MatchesFrom" which is marked as @internal
//
// @public
export function buildView<TMachine extends AnyStateMachine, TEvent extends EventObject, TActions, TSelectors extends AnySelector, TSlots extends readonly Slot[] = [], TMatches extends AnyFunction = MatchesFrom<TMachine>, TViewProps = ViewProps<OutputFromSelector<TSelectors>, TActions, TSlots, TMatches>, TSend = (send: TEvent) => void>(__machine: TMachine, __selectors: TSelectors, __actions: (send: TSend, selectors: OutputFromSelector<TSelectors>) => TActions, __slots: TSlots, view: React_2.ComponentType<TViewProps>): React_2.ComponentType<TViewProps>;

// Warning: (ae-forgotten-export) The symbol "InferViewProps" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "PropsOf" needs to be exported by the entry point index.d.ts
//
// @public
export function buildViewProps<C extends keyof JSX.IntrinsicElements | JSXElementConstructor<any>>(_view: C, props: Pick<InferViewProps<PropsOf<C>>, "actions" | "selectors">): InferViewProps<PropsOf<C>>;

// @public
export function buildXStateTreeMachine<TMachine extends AnyStateMachine, TSelectors extends AnySelector, TActions extends AnyActions>(machine: TMachine, meta: XStateTreeMachineMeta<TMachine, TSelectors, TActions>): StateMachine<ContextFrom<TMachine>, XstateTreeMachineStateSchema<TMachine, TSelectors, TActions>, EventFrom<TMachine>, any, any, any, any>;

// @public
export const genericSlotsTestingDummy: any;

// @public (undocumented)
export type GetSlotNames<TSlots extends readonly Slot[]> = TSlots[number]["name"];

// @public
export type GlobalEvents = {
    [I in keyof XstateTreeEvents]: XstateTreeEvents[I] extends string ? {
        type: I;
    } : XstateTreeEvents[I] & {
        type: I;
    };
}[keyof XstateTreeEvents];

// Warning: (ae-forgotten-export) The symbol "Options" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "Context" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "Events" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "States" needs to be exported by the entry point index.d.ts
//
// @public
export function lazy<TMachine extends AnyStateMachine>(factory: () => Promise<TMachine>, { Loader, withContext, }?: Options_2<TMachine["context"]>): StateMachine<Context, any, Events, States, any, any, any>;

// @public
export function Link<TRoute extends AnyRoute>({ to, children, testId, ...rest }: LinkProps<TRoute>): JSX.Element;

// @public (undocumented)
export type LinkProps<TRoute extends AnyRoute, TRouteParams = TRoute extends Route<infer TParams, any, any, any> ? TParams : undefined, TRouteQuery = TRoute extends Route<any, infer TQuery, any, any> ? TQuery : undefined, TRouteMeta = TRoute extends Route<any, any, any, infer TMeta> ? TMeta : undefined> = {
    to: TRoute;
    children: React_2.ReactNode;
    testId?: string;
    onClick?: (e: React_2.MouseEvent<HTMLAnchorElement>) => boolean | void;
} & RouteArguments<TRouteParams, TRouteQuery, TRouteMeta> & Omit<React_2.AnchorHTMLAttributes<HTMLAnchorElement>, "href" | "onClick">;

// @public (undocumented)
export function loggingMetaOptions<TEvents extends EventObject, TContext>(ignoredEvents: TEvents["type"][], ignoreContext?: (keyof TContext)[] | undefined): {
    xstateTree: {
        ignoredEvents: Map<string, boolean>;
        ignoreContext: (keyof TContext)[] | undefined;
    };
};

// Warning: (ae-internal-missing-underscore) The name "MatchesFrom" should be prefixed with an underscore because the declaration is marked as @internal
//
// @internal (undocumented)
export type MatchesFrom<T extends AnyStateMachine> = StateFrom<T>["matches"];

// Warning: (ae-forgotten-export) The symbol "Return" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export function matchRoute<TRoutes extends Route<any, any, any, any>[]>(routes: TRoutes, basePath: string, path: string, search: string): Return<TRoutes>;

// @public
export type Meta<T> = T extends {
    meta: infer TMeta;
} ? TMeta : undefined;

// @public (undocumented)
export type MultiSlot<T> = {
    type: SlotType.MultiSlot;
    name: T;
    getId(id: string): string;
};

// @public (undocumented)
export function multiSlot<T extends string>(name: T): MultiSlot<T>;

// @public
export function onBroadcast(handler: (event: GlobalEvents) => void): () => void;

// @public (undocumented)
export type Options<TParamsSchema extends Z.ZodObject<any>, TQuerySchema extends Z.ZodObject<any>, TMetaSchema> = {
    params?: TParamsSchema;
    query?: TQuerySchema;
    meta?: TMetaSchema;
};

// @public (undocumented)
export type OutputFromSelector<T> = T extends Selectors<any, any, infer O, any> ? O : never;

// @public
export type Params<T> = T extends {
    params: infer TParams;
} ? TParams : undefined;

// @public
export type PickEvent<T extends Extract<GlobalEvents, {
    type: string;
}>["type"]> = Extract<GlobalEvents, {
    type: T;
}>;

// @public
export type Query<T> = T extends {
    query: infer TQuery;
} ? TQuery : undefined;

// @public
export type Route<TParams, TQuery, TEvent, TMeta> = {
    matches: (url: string, search: string) => ({
        type: TEvent;
        originalUrl: string;
    } & RouteArguments<TParams, TQuery, TMeta>) | undefined;
    reverse: RouteArgumentFunctions<string, TParams, TQuery, undefined>;
    navigate: RouteArgumentFunctions<void, TParams, TQuery, TMeta>;
    getEvent: RouteArgumentFunctions<{
        type: TEvent;
    } & RouteArguments<TParams, TQuery, TMeta>, TParams, TQuery, TMeta>;
    event: TEvent;
    url?: string;
    history: XstateTreeHistory;
    basePath: string;
    parent?: AnyRoute;
    paramsSchema?: Z.ZodObject<any>;
    querySchema?: Z.ZodObject<any>;
};

// Warning: (ae-forgotten-export) The symbol "IsEmptyObject" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "EmptyRouteArguments" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "MakeEmptyObjectPropertiesOptional" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export type RouteArgumentFunctions<TReturn, TParams, TQuery, TMeta, TArgs = RouteArguments<TParams, TQuery, TMeta>> = IsEmptyObject<TArgs> extends true ? () => TReturn : keyof TArgs extends "meta" ? (args?: TArgs) => TReturn : EmptyRouteArguments<TParams, TQuery> extends true ? (args?: Partial<TArgs>) => TReturn : (args: MakeEmptyObjectPropertiesOptional<TArgs>) => TReturn;

// @public (undocumented)
export type RouteArguments<TParams, TQuery, TMeta> = TParams extends undefined ? TQuery extends undefined ? TMeta extends undefined ? {} : {
    meta?: TMeta;
} : TMeta extends undefined ? {
    query: TQuery;
} : {
    query: TQuery;
    meta?: TMeta;
} : TQuery extends undefined ? TMeta extends undefined ? {
    params: TParams;
} : {
    params: TParams;
    meta?: TMeta;
} : TMeta extends undefined ? {
    params: TParams;
    query: TQuery;
} : {
    params: TParams;
    query: TQuery;
    meta?: TMeta;
};

// @public
export type RouteMeta<T> = T extends Route<any, any, any, infer TMeta> ? TMeta : undefined;

// @public
export type RouteParams<T> = T extends Route<infer TParams, any, any, any> ? TParams : undefined;

// @public (undocumented)
export type Routing404Event = {
    type: "ROUTING_404";
    url: string;
};

// @public
export type RoutingEvent<T> = T extends Route<infer TParams, infer TQuery, infer TEvent, infer TMeta> ? {
    type: TEvent;
    originalUrl: string;
    params: TParams;
    query: TQuery;
    meta: TMeta;
} : never;

// @public (undocumented)
export type Selectors<TContext, TEvent, TSelectors, TMatches> = (ctx: TContext, canHandleEvent: (e: TEvent) => boolean, inState: TMatches, __currentState: never) => TSelectors;

// @public (undocumented)
export type SharedMeta = {
    doNotNotifyReactRouter?: boolean;
    indexEvent?: boolean;
    replace?: boolean;
    onloadEvent?: boolean;
};

// @public (undocumented)
export type SingleSlot<T> = {
    type: SlotType.SingleSlot;
    name: T;
    getId(): string;
};

// @public (undocumented)
export function singleSlot<T extends string>(name: T): SingleSlot<T>;

// @public (undocumented)
export type Slot = SingleSlot<any> | MultiSlot<any>;

// @public
export function slotTestingDummyFactory(name: string): StateMachine<unknown, XstateTreeMachineStateSchema<StateMachine<unknown, any, AnyEventObject, {
    value: any;
    context: unknown;
}, BaseActionObject, ServiceMap, ResolveTypegenMeta<TypegenDisabled, AnyEventObject, BaseActionObject, ServiceMap>>, () => {}, () => {}>, AnyEventObject, any, any, any, any>;

// @public (undocumented)
export enum SlotType {
    // (undocumented)
    MultiSlot = 1,
    // (undocumented)
    SingleSlot = 0
}

// @public (undocumented)
export type StyledLink<TStyleProps = {}> = <TRoute extends AnyRoute>(props: LinkProps<TRoute> & TStyleProps) => JSX.Element;

// @public (undocumented)
export type ViewProps<TSelectors, TActions, TSlots extends readonly Slot[], TMatches extends AnyFunction> = {
    slots: Record<GetSlotNames<TSlots>, React_2.ComponentType>;
    actions: TActions;
    selectors: TSelectors;
    inState: TMatches;
};

// @public (undocumented)
export type XstateTreeHistory<T = unknown> = History_2<{
    meta?: T;
    previousUrl?: string;
}>;

// @public (undocumented)
export type XStateTreeMachineMeta<TMachine extends AnyStateMachine, TSelectors, TActions extends AnyActions, TSlots extends readonly Slot[] = Slot[]> = {
    slots: TSlots;
    view: React_2.ComponentType<ViewProps<OutputFromSelector<TSelectors>, ReturnType<TActions>, TSlots, MatchesFrom<TMachine>>>;
    selectors: TSelectors;
    actions: TActions;
    xstateTreeMachine?: true;
};

// @public (undocumented)
export type XstateTreeMachineStateSchema<TMachine extends AnyStateMachine, TSelectors extends AnySelector, TActions extends AnyActions> = {
    meta: XStateTreeMachineMeta<TMachine, TSelectors, TActions>;
};

// Warnings were encountered during analysis:
//
// src/types.ts:22:3 - (ae-incompatible-release-tags) The symbol "view" is marked as @public, but its signature references "MatchesFrom" which is marked as @internal

// (No @packageDocumentation comment for this package)

```
