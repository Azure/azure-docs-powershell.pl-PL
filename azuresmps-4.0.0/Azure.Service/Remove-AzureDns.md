---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055445"
---
# <span data-ttu-id="24685-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="24685-101">Remove-AzureDns</span></span>

## <span data-ttu-id="24685-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24685-102">SYNOPSIS</span></span>
<span data-ttu-id="24685-103">Usuwa serwer DNS z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24685-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="24685-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24685-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="24685-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24685-105">DESCRIPTION</span></span>
<span data-ttu-id="24685-106">Polecenie cmdlet **Remove-AzureDns** usuwa serwer DNS z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24685-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="24685-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24685-107">EXAMPLES</span></span>

### <span data-ttu-id="24685-108">Przykład 1: Usuwanie serwera DNS z usługi</span><span class="sxs-lookup"><span data-stu-id="24685-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="24685-109">To polecenie usuwa serwer DNS o nazwie Dns07 z ContosoService.</span><span class="sxs-lookup"><span data-stu-id="24685-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="24685-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24685-110">PARAMETERS</span></span>

### <span data-ttu-id="24685-111">-Force</span><span class="sxs-lookup"><span data-stu-id="24685-111">-Force</span></span>
<span data-ttu-id="24685-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="24685-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24685-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="24685-113">-InformationAction</span></span>
<span data-ttu-id="24685-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="24685-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="24685-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="24685-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24685-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="24685-116">Continue</span></span>
- <span data-ttu-id="24685-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="24685-117">Ignore</span></span>
- <span data-ttu-id="24685-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="24685-118">Inquire</span></span>
- <span data-ttu-id="24685-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="24685-119">SilentlyContinue</span></span>
- <span data-ttu-id="24685-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="24685-120">Stop</span></span>
- <span data-ttu-id="24685-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="24685-121">Suspend</span></span>

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

### <span data-ttu-id="24685-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="24685-122">-InformationVariable</span></span>
<span data-ttu-id="24685-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="24685-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="24685-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24685-124">-Name</span></span>
<span data-ttu-id="24685-125">Określa nazwę serwera DNS, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24685-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="24685-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="24685-126">-Profile</span></span>
<span data-ttu-id="24685-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24685-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="24685-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="24685-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="24685-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="24685-129">-ServiceName</span></span>
<span data-ttu-id="24685-130">Określa nazwę usługi, z poziomu której to polecenie cmdlet usuwa serwer DNS.</span><span class="sxs-lookup"><span data-stu-id="24685-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="24685-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24685-131">CommonParameters</span></span>
<span data-ttu-id="24685-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24685-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24685-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24685-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24685-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24685-134">INPUTS</span></span>

## <span data-ttu-id="24685-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24685-135">OUTPUTS</span></span>

### <span data-ttu-id="24685-136">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="24685-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="24685-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24685-137">NOTES</span></span>

## <span data-ttu-id="24685-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24685-138">RELATED LINKS</span></span>

[<span data-ttu-id="24685-139">Dodaj-AzureDns</span><span class="sxs-lookup"><span data-stu-id="24685-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="24685-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="24685-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="24685-141">Nowe — AzureDns</span><span class="sxs-lookup"><span data-stu-id="24685-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="24685-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="24685-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


