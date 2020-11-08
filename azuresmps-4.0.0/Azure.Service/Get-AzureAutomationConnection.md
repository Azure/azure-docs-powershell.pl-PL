---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055336"
---
# <span data-ttu-id="cdfe8-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdfe8-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="cdfe8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdfe8-102">SYNOPSIS</span></span>

<span data-ttu-id="cdfe8-103">Pobiera połączenie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="cdfe8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdfe8-104">SYNTAX</span></span>

### <span data-ttu-id="cdfe8-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdfe8-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="cdfe8-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="cdfe8-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdfe8-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="cdfe8-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cdfe8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cdfe8-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="cdfe8-109">Polecenie cmdlet **Get-AzureAutomationConnection** pobiera co najmniej jedno połączenie usługi Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="cdfe8-110">Domyślnie zostaną zwrócone wszystkie połączenia.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-110">By default, all connections are returned.</span></span>
<span data-ttu-id="cdfe8-111">Aby uzyskać określone połączenie, określ jego nazwę.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="cdfe8-112">Aby uzyskać dostęp do wszystkich połączeń określonego typu, określ nazwę typu połączenia.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="cdfe8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdfe8-113">EXAMPLES</span></span>

### <span data-ttu-id="cdfe8-114">Przykład 1: Uzyskaj wszystkie połączenia</span><span class="sxs-lookup"><span data-stu-id="cdfe8-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cdfe8-115">To polecenie pobiera wszystkie połączenia z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cdfe8-116">Przykład 2: uzyskiwanie wszystkich połączeń typu</span><span class="sxs-lookup"><span data-stu-id="cdfe8-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="cdfe8-117">To polecenie pobiera wszystkie połączenia platformy Azure z konta usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cdfe8-118">Przykład 3: uzyskiwanie połączenia</span><span class="sxs-lookup"><span data-stu-id="cdfe8-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="cdfe8-119">To polecenie uzyskuje połączenie o nazwie "Moje połączenie".</span><span class="sxs-lookup"><span data-stu-id="cdfe8-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="cdfe8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdfe8-120">PARAMETERS</span></span>

### <span data-ttu-id="cdfe8-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cdfe8-121">-AutomationAccountName</span></span>
<span data-ttu-id="cdfe8-122">Określa nazwę konta automatyzacji z połączeniem, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="cdfe8-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="cdfe8-123">-ConnectionTypeName</span></span>
<span data-ttu-id="cdfe8-124">Określa nazwę typu połączenia, dla którego mają być pobierane połączenia.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfe8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cdfe8-125">-Name</span></span>
<span data-ttu-id="cdfe8-126">Określa nazwę połączenia, które ma zostać pobrane.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdfe8-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="cdfe8-127">-Profile</span></span>
<span data-ttu-id="cdfe8-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cdfe8-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cdfe8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfe8-130">CommonParameters</span></span>
<span data-ttu-id="cdfe8-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfe8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfe8-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfe8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfe8-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdfe8-133">INPUTS</span></span>

## <span data-ttu-id="cdfe8-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdfe8-134">OUTPUTS</span></span>

### <span data-ttu-id="cdfe8-135">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="cdfe8-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="cdfe8-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdfe8-136">NOTES</span></span>

## <span data-ttu-id="cdfe8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdfe8-137">RELATED LINKS</span></span>

[<span data-ttu-id="cdfe8-138">Nowe — AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdfe8-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="cdfe8-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="cdfe8-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="cdfe8-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="cdfe8-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


