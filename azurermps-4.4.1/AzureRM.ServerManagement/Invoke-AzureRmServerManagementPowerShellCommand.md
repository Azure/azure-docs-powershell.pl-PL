---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546040"
---
# <span data-ttu-id="f8b0c-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="f8b0c-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="f8b0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f8b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b0c-103">Wykonuje blok skryptu programu Windows PowerShell w węźle.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8b0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f8b0c-104">SYNTAX</span></span>

### <span data-ttu-id="f8b0c-105">ByName</span><span class="sxs-lookup"><span data-stu-id="f8b0c-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8b0c-106">BySession</span><span class="sxs-lookup"><span data-stu-id="f8b0c-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b0c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f8b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="f8b0c-108">Polecenie cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** wykonuje blok skryptu programu Windows PowerShell w węźle zarządzanym przez bramę zarządzania programu Azure Server.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="f8b0c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f8b0c-109">EXAMPLES</span></span>

## <span data-ttu-id="f8b0c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f8b0c-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b0c-111">-Command</span><span class="sxs-lookup"><span data-stu-id="f8b0c-111">-Command</span></span>
<span data-ttu-id="f8b0c-112">Określa blok skryptu, który ma być uruchomiony w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b0c-113">-Nodename</span><span class="sxs-lookup"><span data-stu-id="f8b0c-113">-NodeName</span></span>
<span data-ttu-id="f8b0c-114">Określa nazwę węzła, na którym ma być uruchomiony blok skryptu.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-114">Specifies the name of the node to run the script block on.</span></span>

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

### <span data-ttu-id="f8b0c-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="f8b0c-115">-PowerShellSessionName</span></span>
<span data-ttu-id="f8b0c-116">Określa nazwę miejsca uruchamiania programu Windows PowerShell w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

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

### <span data-ttu-id="f8b0c-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="f8b0c-117">-RawOutput</span></span>
<span data-ttu-id="f8b0c-118">Wskazuje, że polecenie cmdlet zwraca pełny obiekt, który zawiera dane wyjściowe z węzła.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8b0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8b0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8b0c-120">Określa nazwę grupy zasobów, do której należy węzeł.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-120">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="f8b0c-121">-Session</span><span class="sxs-lookup"><span data-stu-id="f8b0c-121">-Session</span></span>
<span data-ttu-id="f8b0c-122">Określa obiekt **Session** , którego używa polecenie cmdlet w celu nawiązania połączenia z węzłem docelowym.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="f8b0c-123">Ten parametr można określić zamiast parametrów *ResourceGroupName* , *nodename* , *nazwa_sesji* i *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="f8b0c-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8b0c-124">-Nazwa_sesji</span><span class="sxs-lookup"><span data-stu-id="f8b0c-124">-SessionName</span></span>
<span data-ttu-id="f8b0c-125">Określa nazwę sesji, która ma zarządzać węzłem.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-125">Specifies the name of the session to manage the node.</span></span>

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

### <span data-ttu-id="f8b0c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b0c-126">-DefaultProfile</span></span>
<span data-ttu-id="f8b0c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b0c-128">CommonParameters</span></span>
<span data-ttu-id="f8b0c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b0c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b0c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b0c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8b0c-131">INPUTS</span></span>

### <span data-ttu-id="f8b0c-132">Wielu</span><span class="sxs-lookup"><span data-stu-id="f8b0c-132">Session</span></span>
<span data-ttu-id="f8b0c-133">Parametr "Session" przyjmuje wartość typu "Session" z procesu</span><span class="sxs-lookup"><span data-stu-id="f8b0c-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="f8b0c-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f8b0c-134">OUTPUTS</span></span>

### <span data-ttu-id="f8b0c-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="f8b0c-135">System.Object</span></span>

## <span data-ttu-id="f8b0c-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f8b0c-136">NOTES</span></span>

## <span data-ttu-id="f8b0c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8b0c-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8b0c-138">Polecenia cmdlet zarządzania serwerem Azure</span><span class="sxs-lookup"><span data-stu-id="f8b0c-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


