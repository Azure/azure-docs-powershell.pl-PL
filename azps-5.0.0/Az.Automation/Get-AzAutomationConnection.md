---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225103"
---
# <span data-ttu-id="6c4d2-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6c4d2-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="6c4d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4d2-103">Uzyskuje połączenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="6c4d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c4d2-104">SYNTAX</span></span>

### <span data-ttu-id="6c4d2-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6c4d2-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c4d2-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="6c4d2-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c4d2-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6c4d2-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c4d2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6c4d2-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4d2-109">Polecenie cmdlet **Get-AzAutomationConnection** pobiera co najmniej jedno połączenie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="6c4d2-110">Domyślnie to polecenie cmdlet pobiera wszystkie połączenia.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="6c4d2-111">Określ nazwę połączenia, aby uzyskać określone połączenie.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="6c4d2-112">Określ nazwę typu połączenia, aby uzyskać dostęp do wszystkich połączeń określonego typu.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="6c4d2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c4d2-113">EXAMPLES</span></span>

### <span data-ttu-id="6c4d2-114">Przykład 1: Uzyskaj wszystkie połączenia</span><span class="sxs-lookup"><span data-stu-id="6c4d2-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6c4d2-115">To polecenie pobiera metadane wszystkich połączeń na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6c4d2-116">Przykład 2: uzyskiwanie wszystkich połączeń typu</span><span class="sxs-lookup"><span data-stu-id="6c4d2-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="6c4d2-117">To polecenie pobiera metadane połączeń z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="6c4d2-118">To polecenie pobiera połączenia typu SqlServer.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="6c4d2-119">Przykład 3: uzyskiwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="6c4d2-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="6c4d2-120">To polecenie pobiera metadane połączenia o nazwie ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="6c4d2-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c4d2-121">PARAMETERS</span></span>

### <span data-ttu-id="6c4d2-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c4d2-122">-AutomationAccountName</span></span>
<span data-ttu-id="6c4d2-123">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4d2-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6c4d2-124">-ConnectionTypeName</span></span>
<span data-ttu-id="6c4d2-125">Określa nazwę typu połączenia, dla którego to polecenie cmdlet pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4d2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4d2-126">-DefaultProfile</span></span>
<span data-ttu-id="6c4d2-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6c4d2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c4d2-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6c4d2-128">-Name</span></span>
<span data-ttu-id="6c4d2-129">Określa nazwę połączenia pobieranego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c4d2-131">Określa nazwę grupy zasobów, dla której ten aplet polecenia pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4d2-132">CommonParameters</span></span>
<span data-ttu-id="6c4d2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4d2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c4d2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4d2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c4d2-135">INPUTS</span></span>

### <span data-ttu-id="6c4d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c4d2-136">System.String</span></span>

## <span data-ttu-id="6c4d2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c4d2-137">OUTPUTS</span></span>

### <span data-ttu-id="6c4d2-138">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="6c4d2-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6c4d2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c4d2-139">NOTES</span></span>

## <span data-ttu-id="6c4d2-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c4d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="6c4d2-141">Nowe — AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6c4d2-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="6c4d2-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6c4d2-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


