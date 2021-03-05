---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: f63b27c19b2ba1366b1418360a731829041f5247
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983089"
---
# <span data-ttu-id="d2800-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d2800-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="d2800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2800-102">SYNOPSIS</span></span>
<span data-ttu-id="d2800-103">Usuwa przypisanie do rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d2800-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="d2800-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2800-104">SYNTAX</span></span>

### <span data-ttu-id="d2800-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2800-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [-Scope <String>] -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2800-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d2800-106">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2800-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2800-107">DESCRIPTION</span></span>
<span data-ttu-id="d2800-108">Usuwa przypisanie do rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d2800-108">Deletes a registration assignment.</span></span>

## <span data-ttu-id="d2800-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2800-109">EXAMPLES</span></span>

### <span data-ttu-id="d2800-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2800-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80
PS C:\>
```

<span data-ttu-id="d2800-111">Usuwa zadanie rejestracji według nazwy w domyślnym zakresie.</span><span class="sxs-lookup"><span data-stu-id="d2800-111">Deletes the registration assignment by name at the default scope.</span></span>

### <span data-ttu-id="d2800-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d2800-112">Example 2</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 12b05f0f-3426-48da-9e67-738e1dbf775f
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
PS C:\>
```

<span data-ttu-id="d2800-113">Usuwa przypisanie rejestracji przy użyciu podanego obiektu wejściowego.</span><span class="sxs-lookup"><span data-stu-id="d2800-113">Deletes the registration assignment using the input object provided.</span></span>

### <span data-ttu-id="d2800-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d2800-114">Example 3</span></span>
```
PS C:\> $auths = @(
>>   [Microsoft.Azure.Management.ManagedServices.Models.Authorization]@{RoleDefinitionId = "acdd72a7-3385-48ef-bd42-f606fba81ae7"; PrincipalId = "714160ec-87d5-42bb-8b17-287c0dd7417d" }
>>  );
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -Authorization $auths
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinition $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
b279ec53-b42f-4952-bd62-cd49982e9572 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/b279ec53-b42f-4952-bd62-cd49982e9572 Succeeded


PS C:\> Remove-AzManagedServicesAssignment -Name b279ec53-b42f-4952-bd62-cd49982e9572 -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8
PS C:\>
```

<span data-ttu-id="d2800-115">Usuwa przypisanie rejestracji według nazwy w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="d2800-115">Deletes the registration assignment by name at the given scope.</span></span>

## <span data-ttu-id="d2800-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2800-116">PARAMETERS</span></span>

### <span data-ttu-id="d2800-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2800-117">-DefaultProfile</span></span>
<span data-ttu-id="d2800-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2800-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2800-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2800-119">-InputObject</span></span>
<span data-ttu-id="d2800-120">Obiekt przydziału rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d2800-120">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2800-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d2800-121">-Name</span></span>
<span data-ttu-id="d2800-122">Unikatowa nazwa Zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d2800-122">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="d2800-123">— Zakres</span><span class="sxs-lookup"><span data-stu-id="d2800-123">-Scope</span></span>
<span data-ttu-id="d2800-124">Zakres przydziału rejestracji.</span><span class="sxs-lookup"><span data-stu-id="d2800-124">The scope of the registration assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2800-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2800-125">-AsJob</span></span>
<span data-ttu-id="d2800-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d2800-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2800-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2800-127">-Confirm</span></span>
<span data-ttu-id="d2800-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2800-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2800-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2800-129">-WhatIf</span></span>
<span data-ttu-id="d2800-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2800-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2800-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2800-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2800-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2800-132">CommonParameters</span></span>
<span data-ttu-id="d2800-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2800-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2800-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2800-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2800-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2800-135">INPUTS</span></span>

### <span data-ttu-id="d2800-136">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="d2800-136">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="d2800-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2800-137">OUTPUTS</span></span>

### <span data-ttu-id="d2800-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="d2800-138">System.Void</span></span>
## <span data-ttu-id="d2800-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2800-139">NOTES</span></span>

## <span data-ttu-id="d2800-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2800-140">RELATED LINKS</span></span>
