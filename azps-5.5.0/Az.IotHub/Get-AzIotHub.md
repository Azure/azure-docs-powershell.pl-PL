---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192442"
---
# <span data-ttu-id="53412-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="53412-101">Get-AzIotHub</span></span>

## <span data-ttu-id="53412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53412-102">SYNOPSIS</span></span>
<span data-ttu-id="53412-103">Pobiera informacje o usłudze IotHub w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="53412-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="53412-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53412-104">SYNTAX</span></span>

### <span data-ttu-id="53412-105">ListIotHubsByResourceGroup (domyślna)</span><span class="sxs-lookup"><span data-stu-id="53412-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53412-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="53412-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53412-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="53412-107">DESCRIPTION</span></span>
<span data-ttu-id="53412-108">Pobiera informacje o usłudze IotHub w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="53412-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="53412-109">Możesz wyświetlić wszystkie wystąpienia aplikacji IotHub w subskrypcji lub filtrować wyniki według grupy zasobów lub określonej nazwy usługi IotHub.</span><span class="sxs-lookup"><span data-stu-id="53412-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="53412-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53412-110">EXAMPLES</span></span>

### <span data-ttu-id="53412-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53412-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="53412-112">Pobiera wszystkie usługi IotHubs w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="53412-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="53412-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="53412-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="53412-114">Pobiera wszystkie usługi IotHub z subskrypcji należącej do grupy zasobów o nazwie "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="53412-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="53412-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="53412-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="53412-116">Pobiera informacje o usłudze IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="53412-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="53412-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53412-117">PARAMETERS</span></span>

### <span data-ttu-id="53412-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53412-118">-DefaultProfile</span></span>
<span data-ttu-id="53412-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="53412-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53412-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="53412-120">-Name</span></span>
<span data-ttu-id="53412-121">Nazwa aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="53412-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53412-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53412-122">-ResourceGroupName</span></span>
<span data-ttu-id="53412-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="53412-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53412-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53412-124">CommonParameters</span></span>
<span data-ttu-id="53412-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53412-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53412-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53412-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53412-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53412-127">INPUTS</span></span>

### <span data-ttu-id="53412-128">System.String</span><span class="sxs-lookup"><span data-stu-id="53412-128">System.String</span></span>

## <span data-ttu-id="53412-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53412-129">OUTPUTS</span></span>

### <span data-ttu-id="53412-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="53412-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="53412-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53412-131">NOTES</span></span>

## <span data-ttu-id="53412-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53412-132">RELATED LINKS</span></span>
