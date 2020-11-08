---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054700"
---
# <span data-ttu-id="dab5d-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="dab5d-101">Add-AzureDns</span></span>

## <span data-ttu-id="dab5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dab5d-102">SYNOPSIS</span></span>
<span data-ttu-id="dab5d-103">Dodaje serwer DNS do usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="dab5d-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="dab5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dab5d-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="dab5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dab5d-105">DESCRIPTION</span></span>
<span data-ttu-id="dab5d-106">Polecenie cmdlet **Add-AzureDns** umożliwia dodanie serwera DNS do usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="dab5d-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="dab5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dab5d-107">EXAMPLES</span></span>

### <span data-ttu-id="dab5d-108">Przykład 1: Dodawanie serwera DNS</span><span class="sxs-lookup"><span data-stu-id="dab5d-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="dab5d-109">To polecenie dodaje serwer DNS o adresie 10.1.2.4 do ContosoService.</span><span class="sxs-lookup"><span data-stu-id="dab5d-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="dab5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dab5d-110">PARAMETERS</span></span>

### <span data-ttu-id="dab5d-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dab5d-111">-InformationAction</span></span>
<span data-ttu-id="dab5d-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="dab5d-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dab5d-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dab5d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dab5d-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="dab5d-114">Continue</span></span>
- <span data-ttu-id="dab5d-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="dab5d-115">Ignore</span></span>
- <span data-ttu-id="dab5d-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="dab5d-116">Inquire</span></span>
- <span data-ttu-id="dab5d-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dab5d-117">SilentlyContinue</span></span>
- <span data-ttu-id="dab5d-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="dab5d-118">Stop</span></span>
- <span data-ttu-id="dab5d-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="dab5d-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab5d-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dab5d-120">-InformationVariable</span></span>
<span data-ttu-id="dab5d-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="dab5d-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab5d-122">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="dab5d-122">-IPAddress</span></span>
<span data-ttu-id="dab5d-123">Określa adres IP serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="dab5d-123">Specifies the IP address of the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab5d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dab5d-124">-Name</span></span>
<span data-ttu-id="dab5d-125">Określa przyjazną nazwę dla serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="dab5d-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="dab5d-126">Ta nazwa nie musi być w pełni kwalifikowaną nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="dab5d-126">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab5d-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="dab5d-127">-Profile</span></span>
<span data-ttu-id="dab5d-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dab5d-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dab5d-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dab5d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dab5d-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dab5d-130">-ServiceName</span></span>
<span data-ttu-id="dab5d-131">Określa nazwę usługi, do której to polecenie cmdlet dodaje serwer DNS.</span><span class="sxs-lookup"><span data-stu-id="dab5d-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dab5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab5d-132">CommonParameters</span></span>
<span data-ttu-id="dab5d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dab5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab5d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dab5d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab5d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dab5d-135">INPUTS</span></span>

## <span data-ttu-id="dab5d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dab5d-136">OUTPUTS</span></span>

### <span data-ttu-id="dab5d-137">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="dab5d-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="dab5d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dab5d-138">NOTES</span></span>

## <span data-ttu-id="dab5d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dab5d-139">RELATED LINKS</span></span>

[<span data-ttu-id="dab5d-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="dab5d-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="dab5d-141">Nowe — AzureDns</span><span class="sxs-lookup"><span data-stu-id="dab5d-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="dab5d-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="dab5d-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="dab5d-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="dab5d-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


