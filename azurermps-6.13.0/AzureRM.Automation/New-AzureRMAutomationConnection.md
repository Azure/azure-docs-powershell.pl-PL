---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: e86e25cb4752bf6899e1a00fcbccb596b64f8482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543964"
---
# <span data-ttu-id="4c0a7-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c0a7-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="4c0a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0a7-103">Umożliwia utworzenie połączenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c0a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c0a7-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c0a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c0a7-105">DESCRIPTION</span></span>
<span data-ttu-id="4c0a7-106">Polecenie cmdlet **New-AzureRmAutomationConnection** tworzy połączenie w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="4c0a7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c0a7-107">EXAMPLES</span></span>

### <span data-ttu-id="4c0a7-108">Przykład 1. Tworzenie połączenia</span><span class="sxs-lookup"><span data-stu-id="4c0a7-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="4c0a7-109">Pierwsze polecenie powoduje przypisanie tabeli skrótów wartości pól do zmiennej $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="4c0a7-110">Drugie polecenie tworzy połączenie platformy Azure o nazwie Connection12 na koncie usługi Automation o nazwie AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4c0a7-111">W poleceniu są używane wartości pól połączenia w $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="4c0a7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c0a7-112">PARAMETERS</span></span>

### <span data-ttu-id="4c0a7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c0a7-113">-AutomationAccountName</span></span>
<span data-ttu-id="4c0a7-114">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4c0a7-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="4c0a7-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="4c0a7-116">Określa tabelę skrótów zawierającą pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="4c0a7-117">Klucze reprezentują pola połączeń dla określonego typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="4c0a7-118">Wartości reprezentują określone wartości każdego pola połączenia dla wystąpienia połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="4c0a7-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="4c0a7-119">-ConnectionTypeName</span></span>
<span data-ttu-id="4c0a7-120">Określa nazwę typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="4c0a7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0a7-121">-DefaultProfile</span></span>
<span data-ttu-id="4c0a7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4c0a7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c0a7-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="4c0a7-123">-Description</span></span>
<span data-ttu-id="4c0a7-124">Określa opis połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="4c0a7-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c0a7-125">-Name</span></span>
<span data-ttu-id="4c0a7-126">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="4c0a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c0a7-128">Określa nazwę grupy zasobów, dla której to polecenie cmdlet tworzy połączenie.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="4c0a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0a7-129">CommonParameters</span></span>
<span data-ttu-id="4c0a7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0a7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0a7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c0a7-132">INPUTS</span></span>

### <span data-ttu-id="4c0a7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4c0a7-133">System.String</span></span>

### <span data-ttu-id="4c0a7-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="4c0a7-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="4c0a7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c0a7-135">OUTPUTS</span></span>

### <span data-ttu-id="4c0a7-136">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="4c0a7-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4c0a7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c0a7-137">NOTES</span></span>

## <span data-ttu-id="4c0a7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c0a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c0a7-139">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c0a7-139">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="4c0a7-140">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c0a7-140">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


