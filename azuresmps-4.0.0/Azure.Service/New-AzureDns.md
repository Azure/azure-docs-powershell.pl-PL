---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054890"
---
# <span data-ttu-id="5e623-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e623-101">New-AzureDns</span></span>

## <span data-ttu-id="5e623-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e623-102">SYNOPSIS</span></span>
<span data-ttu-id="5e623-103">Tworzy obiekt ustawień DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e623-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="5e623-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e623-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e623-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e623-105">DESCRIPTION</span></span>
<span data-ttu-id="5e623-106">Polecenie cmdlet **New-AzureDns** tworzy obiekt ustawienia DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e623-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="5e623-107">Obiekt ustawienia DNS można wykorzystać podczas tworzenia maszyny wirtualnej za pomocą polecenia cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e623-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="5e623-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e623-108">EXAMPLES</span></span>

### <span data-ttu-id="5e623-109">Przykład 1. Tworzenie obiektu ustawień DNS</span><span class="sxs-lookup"><span data-stu-id="5e623-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="5e623-110">To polecenie tworzy obiekt ustawienia DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5e623-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="5e623-111">Serwer DNS ma określony adres i przyjazną nazwę Dns01.</span><span class="sxs-lookup"><span data-stu-id="5e623-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="5e623-112">Polecenie zapisuje obiekt w zmiennej $Dns w celu użycia go przez polecenie cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e623-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="5e623-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e623-113">PARAMETERS</span></span>

### <span data-ttu-id="5e623-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5e623-114">-InformationAction</span></span>
<span data-ttu-id="5e623-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5e623-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e623-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5e623-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e623-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5e623-117">Continue</span></span>
- <span data-ttu-id="5e623-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5e623-118">Ignore</span></span>
- <span data-ttu-id="5e623-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="5e623-119">Inquire</span></span>
- <span data-ttu-id="5e623-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5e623-120">SilentlyContinue</span></span>
- <span data-ttu-id="5e623-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5e623-121">Stop</span></span>
- <span data-ttu-id="5e623-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5e623-122">Suspend</span></span>

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

### <span data-ttu-id="5e623-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5e623-123">-InformationVariable</span></span>
<span data-ttu-id="5e623-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5e623-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5e623-125">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="5e623-125">-IPAddress</span></span>
<span data-ttu-id="5e623-126">Określa adres IP serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="5e623-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="5e623-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e623-127">-Name</span></span>
<span data-ttu-id="5e623-128">Określa przyjazną nazwę dla serwera DNS.</span><span class="sxs-lookup"><span data-stu-id="5e623-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="5e623-129">Ta nazwa nie musi być w pełni kwalifikowaną nazwą domeny.</span><span class="sxs-lookup"><span data-stu-id="5e623-129">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="5e623-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e623-130">CommonParameters</span></span>
<span data-ttu-id="5e623-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e623-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e623-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e623-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e623-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e623-133">INPUTS</span></span>

## <span data-ttu-id="5e623-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e623-134">OUTPUTS</span></span>

## <span data-ttu-id="5e623-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e623-135">NOTES</span></span>

## <span data-ttu-id="5e623-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e623-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e623-137">Dodaj-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e623-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="5e623-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e623-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="5e623-139">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="5e623-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5e623-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e623-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="5e623-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e623-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


