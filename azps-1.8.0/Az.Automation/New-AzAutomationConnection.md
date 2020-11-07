---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710539"
---
# <span data-ttu-id="a062b-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a062b-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="a062b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a062b-102">SYNOPSIS</span></span>
<span data-ttu-id="a062b-103">Umożliwia utworzenie połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a062b-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="a062b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a062b-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a062b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a062b-105">DESCRIPTION</span></span>
<span data-ttu-id="a062b-106">Polecenie cmdlet **New-AzAutomationConnection** tworzy połączenie w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a062b-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="a062b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a062b-107">EXAMPLES</span></span>

### <span data-ttu-id="a062b-108">Przykład 1. Tworzenie połączenia</span><span class="sxs-lookup"><span data-stu-id="a062b-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a062b-109">Pierwsze polecenie powoduje przypisanie tabeli skrótów wartości pól do zmiennej $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="a062b-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="a062b-110">Drugie polecenie tworzy połączenie platformy Azure o nazwie Connection12 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a062b-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a062b-111">W poleceniu są używane wartości pól połączenia w $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="a062b-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="a062b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a062b-112">PARAMETERS</span></span>

### <span data-ttu-id="a062b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a062b-113">-AutomationAccountName</span></span>
<span data-ttu-id="a062b-114">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="a062b-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a062b-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="a062b-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="a062b-116">Określa tabelę skrótów zawierającą pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="a062b-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="a062b-117">Klucze reprezentują pola połączeń dla określonego typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="a062b-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="a062b-118">Wartości reprezentują określone wartości każdego pola połączenia dla wystąpienia połączenia.</span><span class="sxs-lookup"><span data-stu-id="a062b-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="a062b-119">-ConnectionTypeName</span></span>
<span data-ttu-id="a062b-120">Określa nazwę typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="a062b-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a062b-121">-DefaultProfile</span></span>
<span data-ttu-id="a062b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a062b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a062b-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="a062b-123">-Description</span></span>
<span data-ttu-id="a062b-124">Określa opis połączenia.</span><span class="sxs-lookup"><span data-stu-id="a062b-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="a062b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a062b-125">-Name</span></span>
<span data-ttu-id="a062b-126">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="a062b-126">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a062b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a062b-127">-ResourceGroupName</span></span>
<span data-ttu-id="a062b-128">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="a062b-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="a062b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a062b-129">CommonParameters</span></span>
<span data-ttu-id="a062b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a062b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a062b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a062b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a062b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a062b-132">INPUTS</span></span>

### <span data-ttu-id="a062b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a062b-133">System.String</span></span>

### <span data-ttu-id="a062b-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="a062b-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="a062b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a062b-135">OUTPUTS</span></span>

### <span data-ttu-id="a062b-136">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="a062b-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="a062b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a062b-137">NOTES</span></span>

## <span data-ttu-id="a062b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a062b-138">RELATED LINKS</span></span>

[<span data-ttu-id="a062b-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a062b-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="a062b-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a062b-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


