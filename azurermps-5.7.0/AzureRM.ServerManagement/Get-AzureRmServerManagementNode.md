---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: f33c6b4c7ac1fc0f1b7de11afc8395232c599539
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542319"
---
# <span data-ttu-id="287af-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="287af-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="287af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="287af-102">SYNOPSIS</span></span>
<span data-ttu-id="287af-103">Pobiera jeden lub więcej węzłów zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="287af-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="287af-104">SYNTAX</span></span>

### <span data-ttu-id="287af-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="287af-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="287af-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="287af-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="287af-107">DESCRIPTION</span></span>
<span data-ttu-id="287af-108">Polecenie cmdlet **Get-AzureRmServerManagementNode umożliwia pobranie** co najmniej jednego węzła zarządzania serwerem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="287af-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="287af-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="287af-109">EXAMPLES</span></span>

## <span data-ttu-id="287af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="287af-110">PARAMETERS</span></span>

### <span data-ttu-id="287af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287af-111">-DefaultProfile</span></span>
<span data-ttu-id="287af-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="287af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287af-113">-Node</span><span class="sxs-lookup"><span data-stu-id="287af-113">-Node</span></span>
<span data-ttu-id="287af-114">Określa istniejący węzeł, z którego należy pobrać parametry *ResourceGroupName* i *nodename* .</span><span class="sxs-lookup"><span data-stu-id="287af-114">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="287af-115">-Nodename</span><span class="sxs-lookup"><span data-stu-id="287af-115">-NodeName</span></span>
<span data-ttu-id="287af-116">Określa nazwę węzła, dla którego jest pobierane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287af-116">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287af-117">-ResourceGroupName</span></span>
<span data-ttu-id="287af-118">Określa nazwę grupy zasobów, do której należą węzły.</span><span class="sxs-lookup"><span data-stu-id="287af-118">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287af-119">CommonParameters</span></span>
<span data-ttu-id="287af-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287af-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287af-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287af-122">INPUTS</span></span>

### <span data-ttu-id="287af-123">Węzły</span><span class="sxs-lookup"><span data-stu-id="287af-123">Node</span></span>
<span data-ttu-id="287af-124">Parametr "Node" akceptuje wartość typu "Node" z procesu</span><span class="sxs-lookup"><span data-stu-id="287af-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="287af-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="287af-125">OUTPUTS</span></span>

### <span data-ttu-id="287af-126">Microsoft. Azure. Commands. ServerManagement. model. Node</span><span class="sxs-lookup"><span data-stu-id="287af-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="287af-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="287af-127">NOTES</span></span>

## <span data-ttu-id="287af-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="287af-128">RELATED LINKS</span></span>

[<span data-ttu-id="287af-129">Nowe — AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="287af-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="287af-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="287af-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)

