---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185114"
---
# <span data-ttu-id="3c69a-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="3c69a-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="3c69a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c69a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c69a-103">Uzyskaj dostęp do wszystkich wykrytych serwerów w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="3c69a-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="3c69a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c69a-104">SYNTAX</span></span>

### <span data-ttu-id="3c69a-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3c69a-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c69a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3c69a-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c69a-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="3c69a-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c69a-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="3c69a-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c69a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c69a-109">DESCRIPTION</span></span>
<span data-ttu-id="3c69a-110">Polecenie commandlet serwera migracji platformy Azure pobiera wszystkie serwery w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="3c69a-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="3c69a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c69a-111">EXAMPLES</span></span>

### <span data-ttu-id="3c69a-112">Przykład 1. Lista</span><span class="sxs-lookup"><span data-stu-id="3c69a-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="3c69a-113">Pobierz wszystkie serwery w projekcie migracji.</span><span class="sxs-lookup"><span data-stu-id="3c69a-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="3c69a-114">Przykład 2. Pobierz</span><span class="sxs-lookup"><span data-stu-id="3c69a-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="3c69a-115">Uzyskiwanie serwera w projekcie migracji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3c69a-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="3c69a-116">Nazwa jest unikatowym paramentatorem serwera.</span><span class="sxs-lookup"><span data-stu-id="3c69a-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="3c69a-117">Przykład 3. Lista w urządzeniu</span><span class="sxs-lookup"><span data-stu-id="3c69a-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="3c69a-118">Lista wszystkich serwerów urządzenia w projekcie.</span><span class="sxs-lookup"><span data-stu-id="3c69a-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="3c69a-119">Przykład 4. Uzyskiwanie urządzenia</span><span class="sxs-lookup"><span data-stu-id="3c69a-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="3c69a-120">Uzyskaj serwer dla urządzenia w projekcie.</span><span class="sxs-lookup"><span data-stu-id="3c69a-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="3c69a-121">Nazwa jest unikatowym paramentatorem serwera.</span><span class="sxs-lookup"><span data-stu-id="3c69a-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="3c69a-122">Przykład 5. Lista i filtrowanie według nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="3c69a-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="3c69a-123">Wyświetl serwery w projekcie migracji i filtruj odpowiedzi za pomocą nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="3c69a-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="3c69a-124">Przykład 6. Lista w urządzeniu i filtrowanie według nazwy wyświetlanej</span><span class="sxs-lookup"><span data-stu-id="3c69a-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="3c69a-125">Wyświetl serwery urządzenia w projekcie migracji i filtruj odpowiedzi za pomocą nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="3c69a-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="3c69a-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c69a-126">PARAMETERS</span></span>

### <span data-ttu-id="3c69a-127">- UrządzenieName</span><span class="sxs-lookup"><span data-stu-id="3c69a-127">-ApplianceName</span></span>
<span data-ttu-id="3c69a-128">Określa nazwę urządzenia.</span><span class="sxs-lookup"><span data-stu-id="3c69a-128">Specifies the appliance name.</span></span>
<span data-ttu-id="3c69a-129">To wewnętrznie mapuje witrynę.</span><span class="sxs-lookup"><span data-stu-id="3c69a-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-130">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="3c69a-130">-DisplayName</span></span>
<span data-ttu-id="3c69a-131">Określa nazwę wyświetlaną maszyny V Machine.</span><span class="sxs-lookup"><span data-stu-id="3c69a-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c69a-132">-Name</span></span>
<span data-ttu-id="3c69a-133">Określa nazwę komputera V Machine.</span><span class="sxs-lookup"><span data-stu-id="3c69a-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="3c69a-134">Jest to nazwa wewnętrzna.</span><span class="sxs-lookup"><span data-stu-id="3c69a-134">This is an internal Name.</span></span>
<span data-ttu-id="3c69a-135">W przypadku użytkowników użyj nazwy wyświetlanej.</span><span class="sxs-lookup"><span data-stu-id="3c69a-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-136">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="3c69a-136">-ProjectName</span></span>
<span data-ttu-id="3c69a-137">Określa nazwę migrowania projektu.</span><span class="sxs-lookup"><span data-stu-id="3c69a-137">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c69a-138">-ResourceGroupName</span></span>
<span data-ttu-id="3c69a-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c69a-139">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-140">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c69a-140">-SubscriptionId</span></span>
<span data-ttu-id="3c69a-141">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3c69a-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c69a-142">-Confirm</span></span>
<span data-ttu-id="3c69a-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3c69a-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c69a-144">-WhatIf</span></span>
<span data-ttu-id="3c69a-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c69a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c69a-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="3c69a-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c69a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c69a-147">CommonParameters</span></span>
<span data-ttu-id="3c69a-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c69a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c69a-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c69a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c69a-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c69a-150">INPUTS</span></span>

## <span data-ttu-id="3c69a-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c69a-151">OUTPUTS</span></span>

### <span data-ttu-id="3c69a-152">Microsoft.Azure.PowerShell.cmdlet.migrate.models.api202001.IVShellMachine</span><span class="sxs-lookup"><span data-stu-id="3c69a-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="3c69a-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c69a-153">NOTES</span></span>

<span data-ttu-id="3c69a-154">ALIASY</span><span class="sxs-lookup"><span data-stu-id="3c69a-154">ALIASES</span></span>

## <span data-ttu-id="3c69a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c69a-155">RELATED LINKS</span></span>

