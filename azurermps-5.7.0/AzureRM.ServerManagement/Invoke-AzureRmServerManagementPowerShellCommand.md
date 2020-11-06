---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542308"
---
# <span data-ttu-id="2fac3-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="2fac3-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="2fac3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fac3-102">SYNOPSIS</span></span>
<span data-ttu-id="2fac3-103">Wykonuje blok skryptu programu Windows PowerShell w węźle.</span><span class="sxs-lookup"><span data-stu-id="2fac3-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fac3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fac3-104">SYNTAX</span></span>

### <span data-ttu-id="2fac3-105">ByName</span><span class="sxs-lookup"><span data-stu-id="2fac3-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fac3-106">BySession</span><span class="sxs-lookup"><span data-stu-id="2fac3-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fac3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2fac3-107">DESCRIPTION</span></span>
<span data-ttu-id="2fac3-108">Polecenie cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** wykonuje blok skryptu programu Windows PowerShell w węźle zarządzanym przez bramę zarządzania programu Azure Server.</span><span class="sxs-lookup"><span data-stu-id="2fac3-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="2fac3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fac3-109">EXAMPLES</span></span>

## <span data-ttu-id="2fac3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fac3-110">PARAMETERS</span></span>

### <span data-ttu-id="2fac3-111">-Command</span><span class="sxs-lookup"><span data-stu-id="2fac3-111">-Command</span></span>
<span data-ttu-id="2fac3-112">Określa blok skryptu, który ma być uruchomiony w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="2fac3-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fac3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fac3-113">-DefaultProfile</span></span>
<span data-ttu-id="2fac3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fac3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fac3-115">-Nodename</span><span class="sxs-lookup"><span data-stu-id="2fac3-115">-NodeName</span></span>
<span data-ttu-id="2fac3-116">Określa nazwę węzła, na którym ma być uruchomiony blok skryptu.</span><span class="sxs-lookup"><span data-stu-id="2fac3-116">Specifies the name of the node to run the script block on.</span></span>

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

### <span data-ttu-id="2fac3-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="2fac3-117">-PowerShellSessionName</span></span>
<span data-ttu-id="2fac3-118">Określa nazwę miejsca uruchamiania programu Windows PowerShell w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="2fac3-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fac3-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="2fac3-119">-RawOutput</span></span>
<span data-ttu-id="2fac3-120">Wskazuje, że polecenie cmdlet zwraca pełny obiekt, który zawiera dane wyjściowe z węzła.</span><span class="sxs-lookup"><span data-stu-id="2fac3-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fac3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fac3-121">-ResourceGroupName</span></span>
<span data-ttu-id="2fac3-122">Określa nazwę grupy zasobów, do której należy węzeł.</span><span class="sxs-lookup"><span data-stu-id="2fac3-122">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="2fac3-123">-Session</span><span class="sxs-lookup"><span data-stu-id="2fac3-123">-Session</span></span>
<span data-ttu-id="2fac3-124">Określa obiekt **Session** , którego używa polecenie cmdlet w celu nawiązania połączenia z węzłem docelowym.</span><span class="sxs-lookup"><span data-stu-id="2fac3-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="2fac3-125">Ten parametr można określić zamiast parametrów *ResourceGroupName* , *nodename* , *nazwa_sesji* i *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="2fac3-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

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

### <span data-ttu-id="2fac3-126">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="2fac3-126">-SessionName</span></span>
<span data-ttu-id="2fac3-127">Określa nazwę sesji, która ma zarządzać węzłem.</span><span class="sxs-lookup"><span data-stu-id="2fac3-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fac3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fac3-128">CommonParameters</span></span>
<span data-ttu-id="2fac3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fac3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fac3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fac3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fac3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fac3-131">INPUTS</span></span>

### <span data-ttu-id="2fac3-132">Wielu</span><span class="sxs-lookup"><span data-stu-id="2fac3-132">Session</span></span>
<span data-ttu-id="2fac3-133">Parametr "Session" przyjmuje wartość typu "Session" z procesu</span><span class="sxs-lookup"><span data-stu-id="2fac3-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="2fac3-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fac3-134">OUTPUTS</span></span>

### <span data-ttu-id="2fac3-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="2fac3-135">System.Object</span></span>

## <span data-ttu-id="2fac3-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fac3-136">NOTES</span></span>

## <span data-ttu-id="2fac3-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fac3-137">RELATED LINKS</span></span>

[<span data-ttu-id="2fac3-138">Polecenia cmdlet zarządzania serwerem Azure</span><span class="sxs-lookup"><span data-stu-id="2fac3-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


