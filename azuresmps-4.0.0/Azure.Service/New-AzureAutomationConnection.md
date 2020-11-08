---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055186"
---
# <span data-ttu-id="9c693-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9c693-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="9c693-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c693-102">SYNOPSIS</span></span>

<span data-ttu-id="9c693-103">Tworzy połączenie w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="9c693-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="9c693-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c693-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c693-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c693-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9c693-106">Polecenie cmdlet **New-AzureAutomationConnection** tworzy połączenie w usłudze Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9c693-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9c693-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c693-107">EXAMPLES</span></span>

## <span data-ttu-id="9c693-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c693-108">PARAMETERS</span></span>

### <span data-ttu-id="9c693-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c693-109">-AutomationAccountName</span></span>
<span data-ttu-id="9c693-110">Określa nazwę konta automatyzacji, w którym będzie przechowywane połączenie.</span><span class="sxs-lookup"><span data-stu-id="9c693-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="9c693-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="9c693-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="9c693-112">Określa tabelę skrótów zawierającą pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="9c693-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="9c693-113">Klucze reprezentują pola połączeń określonego typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="9c693-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="9c693-114">Wartości reprezentują określone wartości, które mają być przechowywane dla każdego pola połączenia dla wystąpienia połączenia.</span><span class="sxs-lookup"><span data-stu-id="9c693-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9c693-115">-ConnectionTypeName</span></span>
<span data-ttu-id="9c693-116">Określa nazwę typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="9c693-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="9c693-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="9c693-117">-Description</span></span>
<span data-ttu-id="9c693-118">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9c693-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c693-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c693-119">-Name</span></span>
<span data-ttu-id="9c693-120">Określa nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="9c693-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="9c693-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="9c693-121">-Profile</span></span>
<span data-ttu-id="9c693-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c693-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c693-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9c693-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c693-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c693-124">CommonParameters</span></span>
<span data-ttu-id="9c693-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c693-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c693-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c693-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c693-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c693-127">INPUTS</span></span>

## <span data-ttu-id="9c693-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c693-128">OUTPUTS</span></span>

### <span data-ttu-id="9c693-129">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="9c693-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9c693-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c693-130">NOTES</span></span>

## <span data-ttu-id="9c693-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c693-131">RELATED LINKS</span></span>

[<span data-ttu-id="9c693-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9c693-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="9c693-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9c693-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="9c693-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9c693-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


