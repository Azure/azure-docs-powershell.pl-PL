---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187483"
---
# <span data-ttu-id="89ef1-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="89ef1-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="89ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="89ef1-103">Pobiera konkretne zadanie rejestru lub listę zadań rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="89ef1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="89ef1-104">SYNTAX</span></span>

### <span data-ttu-id="89ef1-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="89ef1-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ef1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="89ef1-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89ef1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="89ef1-107">DESCRIPTION</span></span>
<span data-ttu-id="89ef1-108">Pobiera konkretne zadanie rejestru lub listę zadań rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="89ef1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="89ef1-109">EXAMPLES</span></span>

### <span data-ttu-id="89ef1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="89ef1-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="89ef1-111">Pobiera wszystkie przypisania rejestracji w domyślnym zakresie.</span><span class="sxs-lookup"><span data-stu-id="89ef1-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="89ef1-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="89ef1-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="89ef1-113">Pobiera wszystkie przypisania rejestracji ze szczegółami definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="89ef1-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="89ef1-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="89ef1-115">Otrzymuje zadanie rejestracji według nazwy bez szczegółów definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="89ef1-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="89ef1-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="89ef1-117">Otrzymuje zadanie rejestracji według nazwy ze szczegółami definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="89ef1-118">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="89ef1-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="89ef1-119">Pobiera wszystkie przypisania rejestracji w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="89ef1-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="89ef1-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89ef1-120">PARAMETERS</span></span>

### <span data-ttu-id="89ef1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ef1-121">-DefaultProfile</span></span>
<span data-ttu-id="89ef1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="89ef1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ef1-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="89ef1-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="89ef1-124">Czy mają być dołączane szczegóły definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ef1-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="89ef1-125">-Name</span></span>
<span data-ttu-id="89ef1-126">Unikatowa nazwa Zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ef1-127">— Zakres</span><span class="sxs-lookup"><span data-stu-id="89ef1-127">-Scope</span></span>
<span data-ttu-id="89ef1-128">Zakres utworzenia przydziału rejestracji.</span><span class="sxs-lookup"><span data-stu-id="89ef1-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="89ef1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ef1-129">CommonParameters</span></span>
<span data-ttu-id="89ef1-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89ef1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ef1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89ef1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ef1-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89ef1-132">INPUTS</span></span>

### <span data-ttu-id="89ef1-133">Brak</span><span class="sxs-lookup"><span data-stu-id="89ef1-133">None</span></span>
## <span data-ttu-id="89ef1-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89ef1-134">OUTPUTS</span></span>

### <span data-ttu-id="89ef1-135">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="89ef1-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="89ef1-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="89ef1-136">NOTES</span></span>

## <span data-ttu-id="89ef1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89ef1-137">RELATED LINKS</span></span>
