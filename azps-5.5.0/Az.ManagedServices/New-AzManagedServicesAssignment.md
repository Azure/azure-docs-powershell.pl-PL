---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187474"
---
# <span data-ttu-id="e4bef-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="e4bef-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="e4bef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bef-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bef-103">Tworzy lub aktualizuje zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="e4bef-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e4bef-104">SYNTAX</span></span>

### <span data-ttu-id="e4bef-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e4bef-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4bef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4bef-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bef-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e4bef-107">DESCRIPTION</span></span>
<span data-ttu-id="e4bef-108">Tworzy lub aktualizuje zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="e4bef-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e4bef-109">EXAMPLES</span></span>

### <span data-ttu-id="e4bef-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4bef-110">Example 1</span></span>
```
PS C:\> $definition = Get-AzManagedServicesDefinition
PS C:\> $definition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
55a89269-0347-4a9c-a778-c3f37b9f8672 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 Succeeded

PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\>
```

<span data-ttu-id="e4bef-111">Tworzy przypisanie rejestracji w domyślnym zakresie przy użyciu identyfikatora definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="e4bef-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e4bef-112">Example 2</span></span>
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


PS C:\>
```

<span data-ttu-id="e4bef-113">Tworzy zadanie rejestracji z obiektem definicji rejestracji jako wartością wejściową.</span><span class="sxs-lookup"><span data-stu-id="e4bef-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="e4bef-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e4bef-114">Example 3</span></span>
```
PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded


PS C:\> New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/55a89269-0347-4a9c-a778-c3f37b9f8672 -Name 12b05f0f-3426-48da-9e67-738e1dbf775f

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
12b05f0f-3426-48da-9e67-738e1dbf775f /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/12b05f0f-3426-48da-9e67-738e1dbf775f Succeeded

PS C:\>
```

<span data-ttu-id="e4bef-115">Aktualizuje zadanie rejestracji przy użyciu identyfikatora i nazwy definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="e4bef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4bef-116">PARAMETERS</span></span>

### <span data-ttu-id="e4bef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bef-117">-DefaultProfile</span></span>
<span data-ttu-id="e4bef-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4bef-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e4bef-119">-Name</span></span>
<span data-ttu-id="e4bef-120">Unikatowa nazwa Zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="e4bef-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e4bef-121">-RegistrationDefinition</span></span>
<span data-ttu-id="e4bef-122">Obiekt wejściowy definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-122">The registration definition input object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bef-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e4bef-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="e4bef-124">W pełni kwalifikowany identyfikator zasobu definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-124">The fully qualified resource id of the registration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4bef-125">— Zakres</span><span class="sxs-lookup"><span data-stu-id="e4bef-125">-Scope</span></span>
<span data-ttu-id="e4bef-126">Zakres, w którym należy utworzyć przypisanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="e4bef-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="e4bef-127">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e4bef-127">-AsJob</span></span>
<span data-ttu-id="e4bef-128">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e4bef-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4bef-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4bef-129">-Confirm</span></span>
<span data-ttu-id="e4bef-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4bef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bef-131">-WhatIf</span></span>
<span data-ttu-id="e4bef-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4bef-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e4bef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4bef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bef-134">CommonParameters</span></span>
<span data-ttu-id="e4bef-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bef-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4bef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bef-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4bef-137">INPUTS</span></span>

### <span data-ttu-id="e4bef-138">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="e4bef-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="e4bef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e4bef-139">System.String</span></span>
## <span data-ttu-id="e4bef-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4bef-140">OUTPUTS</span></span>

### <span data-ttu-id="e4bef-141">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="e4bef-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="e4bef-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e4bef-142">NOTES</span></span>

## <span data-ttu-id="e4bef-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4bef-143">RELATED LINKS</span></span>
