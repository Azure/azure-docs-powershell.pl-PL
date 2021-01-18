---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499022"
---
# <span data-ttu-id="c15b3-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="c15b3-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="c15b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c15b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c15b3-103">Pobiera określone zadanie rejestracji lub listę przydziałów rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="c15b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c15b3-104">SYNTAX</span></span>

### <span data-ttu-id="c15b3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c15b3-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c15b3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c15b3-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c15b3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c15b3-107">DESCRIPTION</span></span>
<span data-ttu-id="c15b3-108">Pobiera określone zadanie rejestracji lub listę przydziałów rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="c15b3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c15b3-109">EXAMPLES</span></span>

### <span data-ttu-id="c15b3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c15b3-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c15b3-111">Pobiera wszystkie zadania rejestracji w zakresie domyślnym.</span><span class="sxs-lookup"><span data-stu-id="c15b3-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="c15b3-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c15b3-112">Example 2</span></span>
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

<span data-ttu-id="c15b3-113">Pobiera wszystkie zadania rejestracji ze szczegółami definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="c15b3-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c15b3-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c15b3-115">Pobiera zadanie rejestracji na podstawie nazwy bez szczegółowych informacji o definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="c15b3-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c15b3-116">Example 4</span></span>
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

<span data-ttu-id="c15b3-117">Pobiera przypisanie rejestracji według nazwy ze szczegółami definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="c15b3-118">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="c15b3-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="c15b3-119">Pobiera wszystkie zadania rejestracji w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="c15b3-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="c15b3-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c15b3-120">PARAMETERS</span></span>

### <span data-ttu-id="c15b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15b3-121">-DefaultProfile</span></span>
<span data-ttu-id="c15b3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c15b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c15b3-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="c15b3-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="c15b3-124">Czy uwzględniać szczegóły definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="c15b3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c15b3-125">-Name</span></span>
<span data-ttu-id="c15b3-126">Unikatowa nazwa zadania rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="c15b3-127">-Zakres</span><span class="sxs-lookup"><span data-stu-id="c15b3-127">-Scope</span></span>
<span data-ttu-id="c15b3-128">Zakres, w którym utworzono zadanie rejestracji.</span><span class="sxs-lookup"><span data-stu-id="c15b3-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="c15b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15b3-129">CommonParameters</span></span>
<span data-ttu-id="c15b3-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c15b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15b3-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c15b3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15b3-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c15b3-132">INPUTS</span></span>

### <span data-ttu-id="c15b3-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c15b3-133">None</span></span>
## <span data-ttu-id="c15b3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c15b3-134">OUTPUTS</span></span>

### <span data-ttu-id="c15b3-135">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="c15b3-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="c15b3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c15b3-136">NOTES</span></span>

## <span data-ttu-id="c15b3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c15b3-137">RELATED LINKS</span></span>
