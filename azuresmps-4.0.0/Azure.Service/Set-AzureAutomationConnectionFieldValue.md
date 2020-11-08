---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055393"
---
# <span data-ttu-id="429a0-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="429a0-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="429a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="429a0-102">SYNOPSIS</span></span>

<span data-ttu-id="429a0-103">Modyfikuje wartość pola dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="429a0-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="429a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="429a0-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="429a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="429a0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="429a0-106">Polecenie cmdlet **Set-AzureAutomationConnectionFieldValue** modyfikuje wartość pola dla połączenia w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="429a0-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="429a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="429a0-107">EXAMPLES</span></span>

## <span data-ttu-id="429a0-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="429a0-108">PARAMETERS</span></span>

### <span data-ttu-id="429a0-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="429a0-109">-AutomationAccountName</span></span>
<span data-ttu-id="429a0-110">Określa nazwę konta automatyzacji z połączeniem.</span><span class="sxs-lookup"><span data-stu-id="429a0-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429a0-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="429a0-111">-ConnectionFieldName</span></span>
<span data-ttu-id="429a0-112">Określa nazwę pola.</span><span class="sxs-lookup"><span data-stu-id="429a0-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429a0-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="429a0-113">-Name</span></span>
<span data-ttu-id="429a0-114">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="429a0-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429a0-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="429a0-115">-Profile</span></span>
<span data-ttu-id="429a0-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429a0-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="429a0-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="429a0-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429a0-118">-Value</span><span class="sxs-lookup"><span data-stu-id="429a0-118">-Value</span></span>
<span data-ttu-id="429a0-119">Określa wartość przechowywaną w polu połączenie.</span><span class="sxs-lookup"><span data-stu-id="429a0-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429a0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429a0-120">CommonParameters</span></span>
<span data-ttu-id="429a0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429a0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429a0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="429a0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429a0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="429a0-123">INPUTS</span></span>

## <span data-ttu-id="429a0-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="429a0-124">OUTPUTS</span></span>

## <span data-ttu-id="429a0-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="429a0-125">NOTES</span></span>

## <span data-ttu-id="429a0-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="429a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="429a0-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="429a0-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="429a0-128">Nowe — AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="429a0-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="429a0-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="429a0-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


