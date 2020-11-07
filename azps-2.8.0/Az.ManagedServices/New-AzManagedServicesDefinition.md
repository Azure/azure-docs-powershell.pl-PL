---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesDefinition.md
ms.openlocfilehash: 8bcf260156584ddf7c8c2ac0ec347a59214f20c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704901"
---
# <span data-ttu-id="7dce4-101">New-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7dce4-101">New-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="7dce4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7dce4-102">SYNOPSIS</span></span>
<span data-ttu-id="7dce4-103">Tworzenie lub aktualizowanie definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="7dce4-103">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="7dce4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7dce4-104">SYNTAX</span></span>

### <span data-ttu-id="7dce4-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7dce4-105">Default (Default)</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dce4-106">ByPlan</span><span class="sxs-lookup"><span data-stu-id="7dce4-106">ByPlan</span></span>
```
New-AzManagedServicesDefinition -Name <String> -ManagedByTenantId <String>
 -PrincipalId <String> -RoleDefinitionId <String> [-Description <String>] -PlanName <String>
 -PlanPublisher <String> -PlanProduct <String> -PlanVersion <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dce4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7dce4-107">DESCRIPTION</span></span>
<span data-ttu-id="7dce4-108">Tworzenie lub aktualizowanie definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="7dce4-108">Creates or updates a registration definition.</span></span>

## <span data-ttu-id="7dce4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7dce4-109">EXAMPLES</span></span>

### <span data-ttu-id="7dce4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7dce4-110">Example 1</span></span>
```powershell
PS C:\> PS C:\> New-AzManagedServicesDefinition -Name name -ManagedByTenantId bab3375b-6197-4a15-a44b-16c41faa91d7 -PrincipalId d6f6c88a-5b7a-455e-ba40-ce146d4d3671 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -Description mydef

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fdad02a1-a715-4352-844f-2923233590da bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="7dce4-111">Umożliwia utworzenie lub zaktualizowanie definicji rejestracji pod kątem wymaganych parametrów.</span><span class="sxs-lookup"><span data-stu-id="7dce4-111">Creates or updates a registration definition given the required parameters.</span></span>

### <span data-ttu-id="7dce4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7dce4-112">Example 2</span></span>
```powershell
PS C> New-AzManagedServicesDefinition -Name asd -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7" -PlanName plan -PlanPublisher publisher -PlanProduct product -PlanVersion 0.1

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
8cde7c19-1750-468e-973e-b711549edc35 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="7dce4-113">Umożliwia utworzenie lub zaktualizowanie definicji rejestracji za pomocą szczegółów planu.</span><span class="sxs-lookup"><span data-stu-id="7dce4-113">Creates or updates a registration definition with the plan details.</span></span>

## <span data-ttu-id="7dce4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7dce4-114">PARAMETERS</span></span>

### <span data-ttu-id="7dce4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dce4-115">-AsJob</span></span>
<span data-ttu-id="7dce4-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7dce4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dce4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dce4-117">-DefaultProfile</span></span>
<span data-ttu-id="7dce4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7dce4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dce4-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="7dce4-119">-Description</span></span>
<span data-ttu-id="7dce4-120">Opis definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="7dce4-120">The description of the Registration Definition.</span></span>

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

### <span data-ttu-id="7dce4-121">-ManagedByTenantId</span><span class="sxs-lookup"><span data-stu-id="7dce4-121">-ManagedByTenantId</span></span>
<span data-ttu-id="7dce4-122">Identyfikator dzierżawy ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="7dce4-122">The ManagedBy Tenant Identifier.</span></span>

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

### <span data-ttu-id="7dce4-123">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7dce4-123">-PlanName</span></span>
<span data-ttu-id="7dce4-124">Nazwa planu.</span><span class="sxs-lookup"><span data-stu-id="7dce4-124">The name of the plan.</span></span>

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

### <span data-ttu-id="7dce4-125">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="7dce4-125">-PlanProduct</span></span>
<span data-ttu-id="7dce4-126">Nazwa produktu.</span><span class="sxs-lookup"><span data-stu-id="7dce4-126">The name of the Product.</span></span>

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

### <span data-ttu-id="7dce4-127">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7dce4-127">-PlanPublisher</span></span>
<span data-ttu-id="7dce4-128">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="7dce4-128">The name of the Publisher.</span></span>

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

### <span data-ttu-id="7dce4-129">-PlanVersion</span><span class="sxs-lookup"><span data-stu-id="7dce4-129">-PlanVersion</span></span>
<span data-ttu-id="7dce4-130">Numer wersji planu.</span><span class="sxs-lookup"><span data-stu-id="7dce4-130">The version number of the plan.</span></span>

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

### <span data-ttu-id="7dce4-131">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="7dce4-131">-PrincipalId</span></span>
<span data-ttu-id="7dce4-132">Identyfikator podmiotu zabezpieczeń ManagedBy.</span><span class="sxs-lookup"><span data-stu-id="7dce4-132">The ManagedBy Principal Identifier.</span></span>

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

### <span data-ttu-id="7dce4-133">-RegistrationDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7dce4-133">-RegistrationDefinitionName</span></span>
<span data-ttu-id="7dce4-134">Nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="7dce4-134">The name of the Registration Definition.</span></span>

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

### <span data-ttu-id="7dce4-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7dce4-135">-RoleDefinitionId</span></span>
<span data-ttu-id="7dce4-136">Identyfikator roli zarządzanego dostawcy usług.</span><span class="sxs-lookup"><span data-stu-id="7dce4-136">The Managed Service Provider's Role Identifier.</span></span>

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

### <span data-ttu-id="7dce4-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7dce4-137">-Confirm</span></span>
<span data-ttu-id="7dce4-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dce4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dce4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dce4-139">-WhatIf</span></span>
<span data-ttu-id="7dce4-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dce4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dce4-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7dce4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dce4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dce4-142">CommonParameters</span></span>
<span data-ttu-id="7dce4-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dce4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dce4-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dce4-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dce4-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7dce4-145">INPUTS</span></span>

### <span data-ttu-id="7dce4-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7dce4-146">None</span></span>

## <span data-ttu-id="7dce4-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7dce4-147">OUTPUTS</span></span>

### <span data-ttu-id="7dce4-148">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="7dce4-148">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="7dce4-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7dce4-149">NOTES</span></span>

## <span data-ttu-id="7dce4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7dce4-150">RELATED LINKS</span></span>
