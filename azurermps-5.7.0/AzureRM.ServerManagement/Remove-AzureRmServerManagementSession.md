---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: b2ebde9e6cf0e94e43d41cd75ee7ee09674fc3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550547"
---
# <span data-ttu-id="c79b7-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c79b7-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="c79b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c79b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c79b7-103">Usuwa sesję zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="c79b7-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c79b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c79b7-104">SYNTAX</span></span>

### <span data-ttu-id="c79b7-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c79b7-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c79b7-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c79b7-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c79b7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c79b7-107">DESCRIPTION</span></span>
<span data-ttu-id="c79b7-108">Polecenie cmdlet **Remove-AzureRmServerManagementSession** usuwa sesję zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="c79b7-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="c79b7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c79b7-109">EXAMPLES</span></span>

## <span data-ttu-id="c79b7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c79b7-110">PARAMETERS</span></span>

### <span data-ttu-id="c79b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79b7-111">-DefaultProfile</span></span>
<span data-ttu-id="c79b7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c79b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c79b7-113">-Nodename</span><span class="sxs-lookup"><span data-stu-id="c79b7-113">-NodeName</span></span>
<span data-ttu-id="c79b7-114">Określa nazwę węzła, na którym ten aplet polecenia usunie sesję.</span><span class="sxs-lookup"><span data-stu-id="c79b7-114">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="c79b7-116">Określa nazwę grupy zasobów, do której należy dana sesja.</span><span class="sxs-lookup"><span data-stu-id="c79b7-116">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="c79b7-117">-Session</span><span class="sxs-lookup"><span data-stu-id="c79b7-117">-Session</span></span>
<span data-ttu-id="c79b7-118">Określa sesję, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c79b7-118">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="c79b7-119">Ten parametr może być wykorzystywany zamiast parametrów *ResourceGroupName* , *nodename* i *nazwa_sesji* .</span><span class="sxs-lookup"><span data-stu-id="c79b7-119">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c79b7-120">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="c79b7-120">-SessionName</span></span>
<span data-ttu-id="c79b7-121">Określa nazwę sesji usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c79b7-121">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79b7-122">CommonParameters</span></span>
<span data-ttu-id="c79b7-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c79b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79b7-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79b7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79b7-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c79b7-125">INPUTS</span></span>

### <span data-ttu-id="c79b7-126">Wielu</span><span class="sxs-lookup"><span data-stu-id="c79b7-126">Session</span></span>
<span data-ttu-id="c79b7-127">Parametr "Session" przyjmuje wartość typu "Session" z procesu</span><span class="sxs-lookup"><span data-stu-id="c79b7-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="c79b7-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c79b7-128">OUTPUTS</span></span>

## <span data-ttu-id="c79b7-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c79b7-129">NOTES</span></span>

## <span data-ttu-id="c79b7-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c79b7-130">RELATED LINKS</span></span>

[<span data-ttu-id="c79b7-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c79b7-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="c79b7-132">Nowe — AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="c79b7-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


