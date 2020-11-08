---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: 5282b3d0ae145088cf07040520050937f8d3a335
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231806"
---
# <span data-ttu-id="871d7-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="871d7-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="871d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="871d7-102">SYNOPSIS</span></span>
<span data-ttu-id="871d7-103">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="871d7-103">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="871d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="871d7-104">SYNTAX</span></span>

### <span data-ttu-id="871d7-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="871d7-105">ByName (Default)</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="871d7-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="871d7-106">Default</span></span>
```
Get-AzManagedServicesDefinition [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="871d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="871d7-107">DESCRIPTION</span></span>
<span data-ttu-id="871d7-108">Pobiera określoną definicję rejestracji lub listę definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="871d7-108">Gets a specific registration definition or a list of the registration definitions.</span></span>

## <span data-ttu-id="871d7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="871d7-109">EXAMPLES</span></span>

### <span data-ttu-id="871d7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="871d7-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesDefinition

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="871d7-111">Pobiera wszystkie definicje rejestracji w zakresie domyślnym.</span><span class="sxs-lookup"><span data-stu-id="871d7-111">Gets all registration definitions at default scope.</span></span>

### <span data-ttu-id="871d7-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="871d7-112">Example 2</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="871d7-113">Pobiera definicję rejestracji według nazwy w zakresie domyślnym.</span><span class="sxs-lookup"><span data-stu-id="871d7-113">Gets the registration definition by name at default scope.</span></span>

### <span data-ttu-id="871d7-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="871d7-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesDefinition -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0c146106-c927-4098-a7ca-30bbcf44a502 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502 Succeeded

PS C:\>
```

<span data-ttu-id="871d7-115">Pobiera wszystkie definicje rejestracji w danym zakresie.</span><span class="sxs-lookup"><span data-stu-id="871d7-115">Gets all registration definitions at the given scope.</span></span>

## <span data-ttu-id="871d7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="871d7-116">PARAMETERS</span></span>

### <span data-ttu-id="871d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871d7-117">-DefaultProfile</span></span>
<span data-ttu-id="871d7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="871d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="871d7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="871d7-119">-Name</span></span>
<span data-ttu-id="871d7-120">Unikatowa nazwa definicji rejestracji.</span><span class="sxs-lookup"><span data-stu-id="871d7-120">The unique name of the Registration Definition.</span></span>

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

### <span data-ttu-id="871d7-121">-Zakres</span><span class="sxs-lookup"><span data-stu-id="871d7-121">-Scope</span></span>
<span data-ttu-id="871d7-122">Zakres, w którym utworzono definicję rejestracji.</span><span class="sxs-lookup"><span data-stu-id="871d7-122">The scope where the registration definition created.</span></span>

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

### <span data-ttu-id="871d7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871d7-123">CommonParameters</span></span>
<span data-ttu-id="871d7-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871d7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871d7-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="871d7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871d7-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="871d7-126">INPUTS</span></span>

### <span data-ttu-id="871d7-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="871d7-127">None</span></span>
## <span data-ttu-id="871d7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="871d7-128">OUTPUTS</span></span>

### <span data-ttu-id="871d7-129">Microsoft. Azure. PowerShell. polecenia. ManagedServices. models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="871d7-129">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="871d7-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="871d7-130">NOTES</span></span>

## <span data-ttu-id="871d7-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="871d7-131">RELATED LINKS</span></span>
