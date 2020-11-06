---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: e83a4c71656feb9dbe766339244e54038fa56c84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550131"
---
# <span data-ttu-id="e1f73-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e1f73-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="e1f73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1f73-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f73-103">Uzyskuje połączenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e1f73-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1f73-104">SYNTAX</span></span>

### <span data-ttu-id="e1f73-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1f73-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f73-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="e1f73-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f73-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e1f73-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f73-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e1f73-108">DESCRIPTION</span></span>
<span data-ttu-id="e1f73-109">Polecenie cmdlet **Get-AzureRmAutomationConnection** pobiera co najmniej jedno połączenie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e1f73-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="e1f73-110">Domyślnie to polecenie cmdlet pobiera wszystkie połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1f73-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="e1f73-111">Określ nazwę połączenia, aby uzyskać określone połączenie.</span><span class="sxs-lookup"><span data-stu-id="e1f73-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="e1f73-112">Określ nazwę typu połączenia, aby uzyskać dostęp do wszystkich połączeń określonego typu.</span><span class="sxs-lookup"><span data-stu-id="e1f73-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="e1f73-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1f73-113">EXAMPLES</span></span>

### <span data-ttu-id="e1f73-114">Przykład 1: Uzyskaj wszystkie połączenia</span><span class="sxs-lookup"><span data-stu-id="e1f73-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e1f73-115">To polecenie pobiera metadane wszystkich połączeń na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e1f73-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e1f73-116">Przykład 2: uzyskiwanie wszystkich połączeń typu</span><span class="sxs-lookup"><span data-stu-id="e1f73-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="e1f73-117">To polecenie pobiera metadane połączeń z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e1f73-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e1f73-118">To polecenie pobiera połączenia typu SqlServer.</span><span class="sxs-lookup"><span data-stu-id="e1f73-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="e1f73-119">Przykład 3: uzyskiwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="e1f73-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="e1f73-120">To polecenie pobiera metadane połączenia o nazwie ContosoConnection.</span><span class="sxs-lookup"><span data-stu-id="e1f73-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="e1f73-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1f73-121">PARAMETERS</span></span>

### <span data-ttu-id="e1f73-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1f73-122">-AutomationAccountName</span></span>
<span data-ttu-id="e1f73-123">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1f73-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="e1f73-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e1f73-124">-ConnectionTypeName</span></span>
<span data-ttu-id="e1f73-125">Określa nazwę typu połączenia, dla którego to polecenie cmdlet pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1f73-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

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

### <span data-ttu-id="e1f73-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1f73-126">-Name</span></span>
<span data-ttu-id="e1f73-127">Określa nazwę połączenia pobieranego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1f73-127">Specifies the name of a connection that this cmdlet retrieves.</span></span>

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

### <span data-ttu-id="e1f73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f73-128">-ResourceGroupName</span></span>
<span data-ttu-id="e1f73-129">Określa nazwę grupy zasobów, dla której ten aplet polecenia pobiera połączenia.</span><span class="sxs-lookup"><span data-stu-id="e1f73-129">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="e1f73-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f73-130">-DefaultProfile</span></span>
<span data-ttu-id="e1f73-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f73-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1f73-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f73-132">CommonParameters</span></span>
<span data-ttu-id="e1f73-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f73-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f73-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f73-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f73-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1f73-135">INPUTS</span></span>

## <span data-ttu-id="e1f73-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1f73-136">OUTPUTS</span></span>

### <span data-ttu-id="e1f73-137">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="e1f73-137">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="e1f73-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1f73-138">NOTES</span></span>

## <span data-ttu-id="e1f73-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1f73-139">RELATED LINKS</span></span>

[<span data-ttu-id="e1f73-140">Nowe — AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e1f73-140">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="e1f73-141">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e1f73-141">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


