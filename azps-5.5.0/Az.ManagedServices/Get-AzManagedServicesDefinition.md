---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187482"
---
# <span data-ttu-id="8a591-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8a591-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="8a591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a591-102">SYNOPSIS</span></span>
<span data-ttu-id="8a591-103">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="8a591-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="8a591-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a591-104">SYNTAX</span></span>

### <span data-ttu-id="8a591-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="8a591-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a591-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="8a591-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a591-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a591-107">DESCRIPTION</span></span>
<span data-ttu-id="8a591-108">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="8a591-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="8a591-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a591-109">EXAMPLES</span></span>

### <span data-ttu-id="8a591-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a591-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="8a591-111">Pobiera wszystkie definicje rejestracji w domyślnym zakresie.</span><span class="sxs-lookup"><span data-stu-id="8a591-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="8a591-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8a591-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="8a591-113">Pobiera domyślnie definicję rejestracji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8a591-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="8a591-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8a591-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="8a591-115">Pobiera wszystkie definicje rejestracji w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="8a591-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="8a591-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a591-116">PARAMETERS</span></span>

### <span data-ttu-id="8a591-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a591-117">-DefaultProfile</span></span>
<span data-ttu-id="8a591-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a591-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a591-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a591-119">-Name</span></span>
<span data-ttu-id="8a591-120">Unikatowa nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="8a591-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="8a591-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8a591-121">-Scope</span></span>
<span data-ttu-id="8a591-122">Zakres utworzenia definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="8a591-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="8a591-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a591-123">CommonParameters</span></span>
<span data-ttu-id="8a591-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a591-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a591-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a591-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a591-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a591-126">INPUTS</span></span>

### <span data-ttu-id="8a591-127">Brak</span><span class="sxs-lookup"><span data-stu-id="8a591-127">None</span></span>
## <span data-ttu-id="8a591-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a591-128">OUTPUTS</span></span>

### <span data-ttu-id="8a591-129">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="8a591-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="8a591-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a591-130">NOTES</span></span>

## <span data-ttu-id="8a591-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a591-131">RELATED LINKS</span></span>
