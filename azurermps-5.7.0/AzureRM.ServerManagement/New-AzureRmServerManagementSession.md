---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524930"
---
# <span data-ttu-id="229d3-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="229d3-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="229d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="229d3-102">SYNOPSIS</span></span>
<span data-ttu-id="229d3-103">Tworzy sesję zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="229d3-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="229d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="229d3-104">SYNTAX</span></span>

### <span data-ttu-id="229d3-105">ByName</span><span class="sxs-lookup"><span data-stu-id="229d3-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="229d3-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="229d3-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="229d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="229d3-107">DESCRIPTION</span></span>
<span data-ttu-id="229d3-108">Polecenie cmdlet **New-AzureRmServerManagementSession** tworzy sesję zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="229d3-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="229d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="229d3-109">EXAMPLES</span></span>

## <span data-ttu-id="229d3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="229d3-110">PARAMETERS</span></span>

### <span data-ttu-id="229d3-111">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="229d3-111">-Credential</span></span>
<span data-ttu-id="229d3-112">Określa obiekt **PSCredential** dla połączenia z sesją zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="229d3-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="229d3-113">Aby uzyskać obiekt Credential, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="229d3-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="229d3-114">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="229d3-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229d3-115">-DefaultProfile</span></span>
<span data-ttu-id="229d3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="229d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="229d3-117">-Node</span><span class="sxs-lookup"><span data-stu-id="229d3-117">-Node</span></span>
<span data-ttu-id="229d3-118">Określa węzeł, dla którego zostanie utworzona sesja za pomocą tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="229d3-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="229d3-119">Ten parametr może być wykorzystywany zamiast parametrów *ResourceGroupName* oraz *nodename* .</span><span class="sxs-lookup"><span data-stu-id="229d3-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="229d3-120">-Nodename</span><span class="sxs-lookup"><span data-stu-id="229d3-120">-NodeName</span></span>
<span data-ttu-id="229d3-121">Określa nazwę węzła, dla którego to polecenie cmdlet tworzy sesję.</span><span class="sxs-lookup"><span data-stu-id="229d3-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="229d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="229d3-123">Określa grupę zasobów węzła, dla którego jest tworzona sesja.</span><span class="sxs-lookup"><span data-stu-id="229d3-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229d3-124">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="229d3-124">-SessionName</span></span>
<span data-ttu-id="229d3-125">Określa nazwę, która ma być używana dla sesji.</span><span class="sxs-lookup"><span data-stu-id="229d3-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="229d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229d3-126">CommonParameters</span></span>
<span data-ttu-id="229d3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229d3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="229d3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229d3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="229d3-129">INPUTS</span></span>

### <span data-ttu-id="229d3-130">Węzły</span><span class="sxs-lookup"><span data-stu-id="229d3-130">Node</span></span>
<span data-ttu-id="229d3-131">Parametr "Node" akceptuje wartość typu "Node" z procesu</span><span class="sxs-lookup"><span data-stu-id="229d3-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="229d3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="229d3-132">OUTPUTS</span></span>

### <span data-ttu-id="229d3-133">Microsoft. Azure. Commands. ServerManagement. model. Session</span><span class="sxs-lookup"><span data-stu-id="229d3-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="229d3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="229d3-134">NOTES</span></span>

## <span data-ttu-id="229d3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="229d3-135">RELATED LINKS</span></span>

