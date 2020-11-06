---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546024"
---
# <span data-ttu-id="4fc45-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="4fc45-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="4fc45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fc45-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc45-103">Tworzy węzeł zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="4fc45-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fc45-104">SYNTAX</span></span>

### <span data-ttu-id="4fc45-105">ByName</span><span class="sxs-lookup"><span data-stu-id="4fc45-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc45-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="4fc45-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc45-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4fc45-107">DESCRIPTION</span></span>
<span data-ttu-id="4fc45-108">Polecenie cmdlet **New-AzureRmServerManagementNode** umożliwia utworzenie węzła zarządzania serwerem platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc45-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="4fc45-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fc45-109">EXAMPLES</span></span>

## <span data-ttu-id="4fc45-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fc45-110">PARAMETERS</span></span>

### <span data-ttu-id="4fc45-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="4fc45-111">-ComputerName</span></span>
<span data-ttu-id="4fc45-112">Określa nazwę komputera zarządzanego na komputerze.</span><span class="sxs-lookup"><span data-stu-id="4fc45-112">Specifies the computer name of the computer that is being managed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-113">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="4fc45-113">-Credential</span></span>
<span data-ttu-id="4fc45-114">Określa obiekt **PSCredential** dla połączenia z węzłem zarządzania serwerem.</span><span class="sxs-lookup"><span data-stu-id="4fc45-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="4fc45-115">Aby uzyskać obiekt Credential, użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="4fc45-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="4fc45-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4fc45-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-117">-Gateway</span><span class="sxs-lookup"><span data-stu-id="4fc45-117">-Gateway</span></span>
<span data-ttu-id="4fc45-118">Określa bramę zarządzającą węzłem.</span><span class="sxs-lookup"><span data-stu-id="4fc45-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="4fc45-119">Ten parametr może być wykorzystywany zamiast parametrów *ResourceGroupName* , *gatewayname* i *Location* .</span><span class="sxs-lookup"><span data-stu-id="4fc45-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-120">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="4fc45-120">-GatewayName</span></span>
<span data-ttu-id="4fc45-121">Określa nazwę bramy, która uzyskuje dostęp do węzła.</span><span class="sxs-lookup"><span data-stu-id="4fc45-121">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="4fc45-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4fc45-122">-Location</span></span>
<span data-ttu-id="4fc45-123">Określa lokalizację, w której to polecenie cmdlet tworzy węzeł.</span><span class="sxs-lookup"><span data-stu-id="4fc45-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="4fc45-124">-NodeName</span></span>
<span data-ttu-id="4fc45-125">Określa nazwę węzła.</span><span class="sxs-lookup"><span data-stu-id="4fc45-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc45-126">-ResourceGroupName</span></span>
<span data-ttu-id="4fc45-127">Określa nazwę grupy zasobów, w której ten aplet polecenia tworzy węzeł.</span><span class="sxs-lookup"><span data-stu-id="4fc45-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="4fc45-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="4fc45-128">-Tags</span></span>
<span data-ttu-id="4fc45-129">Określa znaczniki jako pary klucz-wartość.</span><span class="sxs-lookup"><span data-stu-id="4fc45-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc45-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc45-130">-DefaultProfile</span></span>
<span data-ttu-id="4fc45-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc45-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc45-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc45-132">CommonParameters</span></span>
<span data-ttu-id="4fc45-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc45-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc45-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc45-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc45-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fc45-135">INPUTS</span></span>

### <span data-ttu-id="4fc45-136">Problem</span><span class="sxs-lookup"><span data-stu-id="4fc45-136">Gateway</span></span>
<span data-ttu-id="4fc45-137">Parametr "brama" akceptuje wartość typu "brama" z procesu</span><span class="sxs-lookup"><span data-stu-id="4fc45-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="4fc45-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fc45-138">OUTPUTS</span></span>

### <span data-ttu-id="4fc45-139">Microsoft. Azure. Commands. ServerManagement. model. Node</span><span class="sxs-lookup"><span data-stu-id="4fc45-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="4fc45-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fc45-140">NOTES</span></span>

## <span data-ttu-id="4fc45-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fc45-141">RELATED LINKS</span></span>

[<span data-ttu-id="4fc45-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="4fc45-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="4fc45-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="4fc45-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


