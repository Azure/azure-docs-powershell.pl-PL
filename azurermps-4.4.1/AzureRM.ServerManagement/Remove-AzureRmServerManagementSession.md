---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546019"
---
# <span data-ttu-id="0d232-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="0d232-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="0d232-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d232-102">SYNOPSIS</span></span>
<span data-ttu-id="0d232-103">Usuwa sesję zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="0d232-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d232-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d232-104">SYNTAX</span></span>

### <span data-ttu-id="0d232-105">ByName</span><span class="sxs-lookup"><span data-stu-id="0d232-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d232-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="0d232-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d232-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0d232-107">DESCRIPTION</span></span>
<span data-ttu-id="0d232-108">Polecenie cmdlet **Remove-AzureRmServerManagementSession** usuwa sesję zarządzania serwerem Azure.</span><span class="sxs-lookup"><span data-stu-id="0d232-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="0d232-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d232-109">EXAMPLES</span></span>

## <span data-ttu-id="0d232-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d232-110">PARAMETERS</span></span>

### <span data-ttu-id="0d232-111">-Nodename</span><span class="sxs-lookup"><span data-stu-id="0d232-111">-NodeName</span></span>
<span data-ttu-id="0d232-112">Określa nazwę węzła, na którym ten aplet polecenia usunie sesję.</span><span class="sxs-lookup"><span data-stu-id="0d232-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

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

### <span data-ttu-id="0d232-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d232-113">-ResourceGroupName</span></span>
<span data-ttu-id="0d232-114">Określa nazwę grupy zasobów, do której należy dana sesja.</span><span class="sxs-lookup"><span data-stu-id="0d232-114">Specifies the name of the resource group that the session belongs to.</span></span>

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

### <span data-ttu-id="0d232-115">-Session</span><span class="sxs-lookup"><span data-stu-id="0d232-115">-Session</span></span>
<span data-ttu-id="0d232-116">Określa sesję, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d232-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="0d232-117">Ten parametr może być wykorzystywany zamiast parametrów *ResourceGroupName* , *nodename* i *nazwa_sesji* .</span><span class="sxs-lookup"><span data-stu-id="0d232-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d232-118">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="0d232-118">-SessionName</span></span>
<span data-ttu-id="0d232-119">Określa nazwę sesji usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d232-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d232-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d232-120">-DefaultProfile</span></span>
<span data-ttu-id="0d232-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d232-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d232-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d232-122">CommonParameters</span></span>
<span data-ttu-id="0d232-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d232-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d232-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d232-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d232-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d232-125">INPUTS</span></span>

### <span data-ttu-id="0d232-126">Wielu</span><span class="sxs-lookup"><span data-stu-id="0d232-126">Session</span></span>
<span data-ttu-id="0d232-127">Parametr "Session" przyjmuje wartość typu "Session" z procesu</span><span class="sxs-lookup"><span data-stu-id="0d232-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="0d232-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d232-128">OUTPUTS</span></span>

## <span data-ttu-id="0d232-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d232-129">NOTES</span></span>

## <span data-ttu-id="0d232-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d232-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d232-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="0d232-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="0d232-132">Nowe — AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="0d232-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)

