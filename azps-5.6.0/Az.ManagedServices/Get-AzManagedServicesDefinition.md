---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 80c315b5bb2e1a1bcd15a2b9686a1201739171a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010474"
---
# <span data-ttu-id="4cee9-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4cee9-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4cee9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cee9-102">SYNOPSIS</span></span>
<span data-ttu-id="4cee9-103">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cee9-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="4cee9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cee9-104">SYNTAX</span></span>

### <span data-ttu-id="4cee9-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="4cee9-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cee9-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="4cee9-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cee9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cee9-107">DESCRIPTION</span></span>
<span data-ttu-id="4cee9-108">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cee9-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="4cee9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cee9-109">EXAMPLES</span></span>

### <span data-ttu-id="4cee9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4cee9-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="4cee9-111">Pobiera wszystkie definicje rejestracji w domyślnym zakresie.</span><span class="sxs-lookup"><span data-stu-id="4cee9-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="4cee9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4cee9-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="4cee9-113">Pobiera domyślnie definicję rejestracji według nazwy.</span><span class="sxs-lookup"><span data-stu-id="4cee9-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="4cee9-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="4cee9-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="4cee9-115">Pobiera wszystkie definicje rejestracji w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="4cee9-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="4cee9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cee9-116">PARAMETERS</span></span>

### <span data-ttu-id="4cee9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cee9-117">-DefaultProfile</span></span>
<span data-ttu-id="4cee9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cee9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cee9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cee9-119">-Name</span></span>
<span data-ttu-id="4cee9-120">Unikatowa nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cee9-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="4cee9-121">— Zakres</span><span class="sxs-lookup"><span data-stu-id="4cee9-121">-Scope</span></span>
<span data-ttu-id="4cee9-122">Zakres utworzenia definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="4cee9-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="4cee9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cee9-123">CommonParameters</span></span>
<span data-ttu-id="4cee9-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cee9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cee9-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cee9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cee9-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cee9-126">INPUTS</span></span>

### <span data-ttu-id="4cee9-127">Brak</span><span class="sxs-lookup"><span data-stu-id="4cee9-127">None</span></span>
## <span data-ttu-id="4cee9-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cee9-128">OUTPUTS</span></span>

### <span data-ttu-id="4cee9-129">Microsoft.Azure.PowerShell.Cmdlet.ManagedServices.Models.PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="4cee9-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="4cee9-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cee9-130">NOTES</span></span>

## <span data-ttu-id="4cee9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cee9-131">RELATED LINKS</span></span>
