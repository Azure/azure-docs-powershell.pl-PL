---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/new-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/New-AzManagedServicesAssignment.md
ms.openlocfilehash: 8023dde9253ccb4a1f7ff223c4dfdddf773a4728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231804"
---
# <span data-ttu-id="1fff9-101">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="1fff9-101">New-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="1fff9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fff9-102">SYNOPSIS</span></span>
<span data-ttu-id="1fff9-103">Umożliwia utworzenie lub zaktualizowanie zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-103">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="1fff9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fff9-104">SYNTAX</span></span>

### <span data-ttu-id="1fff9-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1fff9-105">Default (Default)</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>] -RegistrationDefinitionId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fff9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1fff9-106">ByInputObject</span></span>
```
New-AzManagedServicesAssignment [-Name <String>] [-Scope <String>]
 -RegistrationDefinition <PSRegistrationDefinition> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fff9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1fff9-107">DESCRIPTION</span></span>
<span data-ttu-id="1fff9-108">Umożliwia utworzenie lub zaktualizowanie zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-108">Creates or updates a registration assignment.</span></span>

## <span data-ttu-id="1fff9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fff9-109">EXAMPLES</span></span>

### <span data-ttu-id="1fff9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fff9-110">Example 1</span></span>
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

<span data-ttu-id="1fff9-111">Tworzy przypisanie rejestracji w zakresie domyślnym przy użyciu identyfikatora definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-111">Creates a registration assignment at the default scope using the registration definition identifier.</span></span>

### <span data-ttu-id="1fff9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1fff9-112">Example 2</span></span>
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

<span data-ttu-id="1fff9-113">Tworzy zadanie rejestracji z obiektem definicji rejestracji jako wejściem.</span><span class="sxs-lookup"><span data-stu-id="1fff9-113">Creates a registration assignment with a registration definition object as input.</span></span>

### <span data-ttu-id="1fff9-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1fff9-114">Example 3</span></span>
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

<span data-ttu-id="1fff9-115">Aktualizuje przydział rejestracji za pomocą identyfikatora i nazwy definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-115">Updates a registration assignment with a registration definition identifier and name.</span></span>


## <span data-ttu-id="1fff9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fff9-116">PARAMETERS</span></span>

### <span data-ttu-id="1fff9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fff9-117">-DefaultProfile</span></span>
<span data-ttu-id="1fff9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fff9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fff9-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1fff9-119">-Name</span></span>
<span data-ttu-id="1fff9-120">Unikatowa nazwa zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-120">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="1fff9-121">-RegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1fff9-121">-RegistrationDefinition</span></span>
<span data-ttu-id="1fff9-122">Obiekt wejściowy definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-122">The registration definition input object.</span></span>

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

### <span data-ttu-id="1fff9-123">-RegistrationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="1fff9-123">-RegistrationDefinitionId</span></span>
<span data-ttu-id="1fff9-124">W pełni kwalifikowany identyfikator zasobu definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-124">The fully qualified resource id of the registration definition.</span></span>

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

### <span data-ttu-id="1fff9-125">-Zakres</span><span class="sxs-lookup"><span data-stu-id="1fff9-125">-Scope</span></span>
<span data-ttu-id="1fff9-126">Zakres, w którym ma zostać utworzony przydział rejestracji.</span><span class="sxs-lookup"><span data-stu-id="1fff9-126">The scope where the registration assignment should be created.</span></span>

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

### <span data-ttu-id="1fff9-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fff9-127">-AsJob</span></span>
<span data-ttu-id="1fff9-128">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1fff9-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fff9-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fff9-129">-Confirm</span></span>
<span data-ttu-id="1fff9-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fff9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fff9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fff9-131">-WhatIf</span></span>
<span data-ttu-id="1fff9-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fff9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fff9-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fff9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fff9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fff9-134">CommonParameters</span></span>
<span data-ttu-id="1fff9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fff9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fff9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fff9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fff9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fff9-137">INPUTS</span></span>

### <span data-ttu-id="1fff9-138">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="1fff9-138">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
### <span data-ttu-id="1fff9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1fff9-139">System.String</span></span>
## <span data-ttu-id="1fff9-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fff9-140">OUTPUTS</span></span>

### <span data-ttu-id="1fff9-141">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="1fff9-141">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="1fff9-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fff9-142">NOTES</span></span>

## <span data-ttu-id="1fff9-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fff9-143">RELATED LINKS</span></span>
