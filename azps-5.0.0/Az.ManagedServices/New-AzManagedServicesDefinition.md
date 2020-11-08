---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: f8d2eded01e4816b99b71475aca896c697dd5ae0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231805"
---
# <span data-ttu-id="45bef-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="45bef-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="45bef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45bef-102">SYNOPSIS</span></span>
<span data-ttu-id="45bef-103">Tworzenie lub aktualizowanie definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="45bef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45bef-104">SYNTAX</span></span>

### <span data-ttu-id="45bef-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="45bef-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -PrincipalId <String> -RoleDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45bef-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="45bef-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> -PlanName <String> -PlanPublisher <String>
 -PlanProduct <String> -PlanVersion <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45bef-107">ByAuthorization</span><span class="sxs-lookup"><span data-stu-id="45bef-107">ByAuthorization</span></span>
```
New-AzManagedServicesDefinition [-Name <String>] -DisplayName <String> -ManagedByTenantId <String>
 [-Description <String>] -Authorization <Authorization[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45bef-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45bef-108">DESCRIPTION</span></span>
<span data-ttu-id="45bef-109">Tworzenie lub aktualizowanie definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-109">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="45bef-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45bef-110">EXAMPLES</span></span>

### <span data-ttu-id="45bef-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45bef-111">Example 1</span></span>
```
PS C:\> New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b732e39c-c034-44cd-b5a1-094669ccc8c5 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/b732e39c-c034-44cd-b5a1-094669ccc8c5 Succeeded


PS C:\>
```

<span data-ttu-id="45bef-112">Tworzy definicję rejestracji według roleDefinitionId i principalId wartości podanych bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="45bef-112">Creates a registration definition by roleDefinitionId and principalId values given directly.</span></span>

### <span data-ttu-id="45bef-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="45bef-113">Example 2</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\>
```

<span data-ttu-id="45bef-114">Umożliwia utworzenie lub zaktualizowanie definicji rejestracji za pomocą szczegółów autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="45bef-114">Creates or updates a registration definition with authorization details.</span></span>

### <span data-ttu-id="45bef-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="45bef-115">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" },
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "9980e02c-c2be-4d73-94e8-173b1dc7cf3c"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7


PS C:\> $definition.Name
55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths -Name 55a89269-0347-4a9c-a778-c3f37b9f8672
PS C:\> $definition.Properties.Authorization

PrincipalId                          RoleDefinitionId
-----------                          ----------------
714160ec-87d5-42bb-8b17-287c0dd7417d acdd72a7-3385-48ef-bd42-f606fba81ae7
714160ec-87d5-42bb-8b17-287c0dd7417d 9980e02c-c2be-4d73-94e8-173b1dc7cf3c

PS C:\>
```

<span data-ttu-id="45bef-116">Aktualizuje definicję rejestracji za pomocą szczegółów autoryzacji i nazwy definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-116">Updates a registration definition with authorization details and name of the registration definition.</span></span>

## <span data-ttu-id="45bef-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45bef-117">PARAMETERS</span></span>

### <span data-ttu-id="45bef-118">— Autoryzacja</span><span class="sxs-lookup"><span data-stu-id="45bef-118">-Authorization</span></span>
<span data-ttu-id="45bef-119">Lista mapowania autoryzacji z principalId-roleDefinitionId.</span><span class="sxs-lookup"><span data-stu-id="45bef-119">The authorization mapping list with principalId - roleDefinitionId.</span></span>

```yaml
Type: Microsoft.Azure.Management.ManagedServices.Models.Authorization[]
Parameter Sets: ByPlan, ByAuthorization
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bef-120">-DefaultProfile</span></span>
<span data-ttu-id="45bef-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45bef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="45bef-122">-Description</span></span>
<span data-ttu-id="45bef-123">Opis definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-123">The description of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="45bef-124">-DisplayName</span></span>
<span data-ttu-id="45bef-125">Nazwa wyświetlana definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-125">The display name of the Registration Definition.</span></span>

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

### <span data-ttu-id="45bef-126">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="45bef-126">-ManagedByTenantId</span></span>
<span data-ttu-id="45bef-127">Identyfikator dzierżawy ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="45bef-127">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="45bef-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45bef-128">-Name</span></span>
<span data-ttu-id="45bef-129">Unikatowa nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="45bef-129">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-130">-PlanName</span><span class="sxs-lookup"><span data-stu-id="45bef-130">-PlanName</span></span>
<span data-ttu-id="45bef-131">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="45bef-131">The name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-132">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="45bef-132">-PlanProduct</span></span>
<span data-ttu-id="45bef-133">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="45bef-133">The name of the Product.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-134">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="45bef-134">-PlanPublisher</span></span>
<span data-ttu-id="45bef-135">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="45bef-135">The name of the Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-136">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="45bef-136">-PlanVersion</span></span>
<span data-ttu-id="45bef-137">Numer wersji planu.</span><span class="sxs-lookup"><span data-stu-id="45bef-137">The version number of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPlan
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-138">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="45bef-138">-PrincipalId</span></span>
<span data-ttu-id="45bef-139">Identyfikator podmiotu zabezpieczeń ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="45bef-139">The ManagedBy Principal Identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-140">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="45bef-140">-RoleDefinitionId</span></span>
<span data-ttu-id="45bef-141">Identyfikator definicji roli umożliwiający udzielenie uprawnień identyfikatorowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="45bef-141">The role definition identifier to grant permissions to principal identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-142">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45bef-142">-AsJob</span></span>
<span data-ttu-id="45bef-143">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="45bef-143">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45bef-144">-Confirm</span></span>
<span data-ttu-id="45bef-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45bef-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bef-146">-WhatIf</span></span>
<span data-ttu-id="45bef-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45bef-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bef-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45bef-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45bef-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bef-149">CommonParameters</span></span>
<span data-ttu-id="45bef-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bef-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bef-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45bef-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bef-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45bef-152">INPUTS</span></span>

### <span data-ttu-id="45bef-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="45bef-153">None</span></span>
## <span data-ttu-id="45bef-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45bef-154">OUTPUTS</span></span>

### <span data-ttu-id="45bef-155">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="45bef-155">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="45bef-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45bef-156">NOTES</span></span>

## <span data-ttu-id="45bef-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45bef-157">RELATED LINKS</span></span>
