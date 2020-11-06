---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546020"
---
# <span data-ttu-id="b031e-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b031e-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="b031e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b031e-102">SYNOPSIS</span></span>
<span data-ttu-id="b031e-103">Umożliwia usunięcie węzła zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="b031e-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b031e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b031e-104">SYNTAX</span></span>

### <span data-ttu-id="b031e-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b031e-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b031e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b031e-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b031e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b031e-107">DESCRIPTION</span></span>
<span data-ttu-id="b031e-108">Polecenie cmdlet **Remove-AzureRmServerManagementNode** usuwa węzeł Zarządzanie serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="b031e-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="b031e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b031e-109">EXAMPLES</span></span>

## <span data-ttu-id="b031e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b031e-110">PARAMETERS</span></span>

### <span data-ttu-id="b031e-111">-Node</span><span class="sxs-lookup"><span data-stu-id="b031e-111">-Node</span></span>
<span data-ttu-id="b031e-112">Określa węzeł, dla którego zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b031e-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="b031e-113">Ten parametr może być wykorzystywany zamiast parametrów *ResourceGroupName* oraz *nodename* .</span><span class="sxs-lookup"><span data-stu-id="b031e-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b031e-114">-Nodename</span><span class="sxs-lookup"><span data-stu-id="b031e-114">-NodeName</span></span>
<span data-ttu-id="b031e-115">Określa nazwę węzła, dla którego zostanie usunięte to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b031e-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b031e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b031e-116">-ResourceGroupName</span></span>
<span data-ttu-id="b031e-117">Określa nazwę grupy zasobów, do której należy węzeł.</span><span class="sxs-lookup"><span data-stu-id="b031e-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b031e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b031e-118">-DefaultProfile</span></span>
<span data-ttu-id="b031e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b031e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b031e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b031e-120">CommonParameters</span></span>
<span data-ttu-id="b031e-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b031e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b031e-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b031e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b031e-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b031e-123">INPUTS</span></span>

### <span data-ttu-id="b031e-124">Węzły</span><span class="sxs-lookup"><span data-stu-id="b031e-124">Node</span></span>
<span data-ttu-id="b031e-125">Parametr "Node" akceptuje wartość typu "Node" z procesu</span><span class="sxs-lookup"><span data-stu-id="b031e-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="b031e-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b031e-126">OUTPUTS</span></span>

## <span data-ttu-id="b031e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b031e-127">NOTES</span></span>

## <span data-ttu-id="b031e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b031e-128">RELATED LINKS</span></span>

[<span data-ttu-id="b031e-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b031e-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="b031e-130">Nowe — AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b031e-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


