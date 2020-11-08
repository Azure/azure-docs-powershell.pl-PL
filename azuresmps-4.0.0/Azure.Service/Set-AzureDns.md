---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055035"
---
# <span data-ttu-id="76f43-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="76f43-101">Set-AzureDns</span></span>

## <span data-ttu-id="76f43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76f43-102">SYNOPSIS</span></span>
<span data-ttu-id="76f43-103">Modyfikuje adres IP serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="76f43-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="76f43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76f43-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="76f43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76f43-105">DESCRIPTION</span></span>
<span data-ttu-id="76f43-106">Polecenie cmdlet **Set-AzureDns** modyfikuje adres IP serwera DNS dla usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="76f43-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="76f43-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76f43-107">EXAMPLES</span></span>

### <span data-ttu-id="76f43-108">Przykład 1. Modyfikowanie adresu IP serwera DNS</span><span class="sxs-lookup"><span data-stu-id="76f43-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="76f43-109">To polecenie modyfikuje adres IP serwera DNS o nazwie Dns07 dla usługi o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="76f43-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="76f43-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76f43-110">PARAMETERS</span></span>

### <span data-ttu-id="76f43-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76f43-111">-InformationAction</span></span>
<span data-ttu-id="76f43-112">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="76f43-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76f43-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="76f43-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76f43-114">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="76f43-114">Continue</span></span>
- <span data-ttu-id="76f43-115">Ignorować</span><span class="sxs-lookup"><span data-stu-id="76f43-115">Ignore</span></span>
- <span data-ttu-id="76f43-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="76f43-116">Inquire</span></span>
- <span data-ttu-id="76f43-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76f43-117">SilentlyContinue</span></span>
- <span data-ttu-id="76f43-118">Przestaw</span><span class="sxs-lookup"><span data-stu-id="76f43-118">Stop</span></span>
- <span data-ttu-id="76f43-119">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="76f43-119">Suspend</span></span>

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

### <span data-ttu-id="76f43-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76f43-120">-InformationVariable</span></span>
<span data-ttu-id="76f43-121">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="76f43-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="76f43-122">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="76f43-122">-IPAddress</span></span>
<span data-ttu-id="76f43-123">Określa nowy adres IP serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="76f43-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="76f43-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76f43-124">-Name</span></span>
<span data-ttu-id="76f43-125">Określa nazwę serwera DNS, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f43-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="76f43-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="76f43-126">-Profile</span></span>
<span data-ttu-id="76f43-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f43-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76f43-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="76f43-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76f43-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="76f43-129">-ServiceName</span></span>
<span data-ttu-id="76f43-130">Określa nazwę usługi, dla której to polecenie cmdlet modyfikuje adres serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="76f43-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="76f43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f43-131">CommonParameters</span></span>
<span data-ttu-id="76f43-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f43-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f43-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f43-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76f43-134">INPUTS</span></span>

## <span data-ttu-id="76f43-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76f43-135">OUTPUTS</span></span>

### <span data-ttu-id="76f43-136">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="76f43-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="76f43-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76f43-137">NOTES</span></span>

## <span data-ttu-id="76f43-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76f43-138">RELATED LINKS</span></span>

[<span data-ttu-id="76f43-139">Dodaj-AzureDns</span><span class="sxs-lookup"><span data-stu-id="76f43-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="76f43-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="76f43-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="76f43-141">Nowe — AzureDns</span><span class="sxs-lookup"><span data-stu-id="76f43-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="76f43-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="76f43-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


