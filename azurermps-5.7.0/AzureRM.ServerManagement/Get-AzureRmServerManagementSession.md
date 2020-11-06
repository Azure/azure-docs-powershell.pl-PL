---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e32f9268309562b45e13df164631e18d28cceb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542316"
---
# <span data-ttu-id="6e313-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="6e313-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="6e313-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e313-102">SYNOPSIS</span></span>
<span data-ttu-id="6e313-103">Pobiera sesję zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="6e313-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e313-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e313-104">SYNTAX</span></span>

### <span data-ttu-id="6e313-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="6e313-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e313-106">BySession</span><span class="sxs-lookup"><span data-stu-id="6e313-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e313-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="6e313-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e313-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6e313-108">DESCRIPTION</span></span>
<span data-ttu-id="6e313-109">Polecenie cmdlet **Get-AzureRmServerManagementSession** pobiera pojedynczą sesję zarządzania serwerem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e313-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="6e313-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e313-110">EXAMPLES</span></span>

## <span data-ttu-id="6e313-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e313-111">PARAMETERS</span></span>

### <span data-ttu-id="6e313-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e313-112">-DefaultProfile</span></span>
<span data-ttu-id="6e313-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e313-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e313-114">-Node</span><span class="sxs-lookup"><span data-stu-id="6e313-114">-Node</span></span>
<span data-ttu-id="6e313-115">Określa istniejący obiekt **Node** , który jest wykorzystywany do pobierania parametrów *ResourceGroupName* i *nodename* .</span><span class="sxs-lookup"><span data-stu-id="6e313-115">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="6e313-116">Należy również określić wartość parametru *SESSIONNAME* .</span><span class="sxs-lookup"><span data-stu-id="6e313-116">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="6e313-117">-Nodename</span><span class="sxs-lookup"><span data-stu-id="6e313-117">-NodeName</span></span>
<span data-ttu-id="6e313-118">Określa nazwę węzła, w którym znajduje się sesja.</span><span class="sxs-lookup"><span data-stu-id="6e313-118">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e313-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e313-119">-ResourceGroupName</span></span>
<span data-ttu-id="6e313-120">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera sesję.</span><span class="sxs-lookup"><span data-stu-id="6e313-120">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e313-121">-Session</span><span class="sxs-lookup"><span data-stu-id="6e313-121">-Session</span></span>
<span data-ttu-id="6e313-122">Określa istniejący obiekt **Session** , który jest wykorzystywany do uzyskiwania *ResourceGroupName* , *nodename* i parametrów *SESSIONNAME* .</span><span class="sxs-lookup"><span data-stu-id="6e313-122">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e313-123">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="6e313-123">-SessionName</span></span>
<span data-ttu-id="6e313-124">Określa nazwę sesji, w której jest pobierany ten aplet polecenia.</span><span class="sxs-lookup"><span data-stu-id="6e313-124">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e313-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e313-125">CommonParameters</span></span>
<span data-ttu-id="6e313-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e313-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e313-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e313-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e313-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e313-128">INPUTS</span></span>

### <span data-ttu-id="6e313-129">Węzły</span><span class="sxs-lookup"><span data-stu-id="6e313-129">Node</span></span>
<span data-ttu-id="6e313-130">Parametr "Node" akceptuje wartość typu "Node" z procesu</span><span class="sxs-lookup"><span data-stu-id="6e313-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="6e313-131">Wielu</span><span class="sxs-lookup"><span data-stu-id="6e313-131">Session</span></span>
<span data-ttu-id="6e313-132">Parametr "Session" przyjmuje wartość typu "Session" z procesu</span><span class="sxs-lookup"><span data-stu-id="6e313-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="6e313-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e313-133">OUTPUTS</span></span>

### <span data-ttu-id="6e313-134">Microsoft. Azure. Commands. ServerManagement. model. Session</span><span class="sxs-lookup"><span data-stu-id="6e313-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="6e313-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e313-135">NOTES</span></span>

## <span data-ttu-id="6e313-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e313-136">RELATED LINKS</span></span>

[<span data-ttu-id="6e313-137">Polecenia cmdlet zarządzania serwerem Azure</span><span class="sxs-lookup"><span data-stu-id="6e313-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


