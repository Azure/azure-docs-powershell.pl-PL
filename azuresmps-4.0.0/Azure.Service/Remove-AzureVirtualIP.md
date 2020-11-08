---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B107D789-8F66-4D7D-B126-08ACB0364826
online version: ''
schema: 2.0.0
ms.openlocfilehash: e59df078539e9ea94073defd4c8ea13a69cc2e5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054453"
---
# <span data-ttu-id="489cf-101">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="489cf-101">Remove-AzureVirtualIP</span></span>

## <span data-ttu-id="489cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="489cf-102">SYNOPSIS</span></span>
<span data-ttu-id="489cf-103">Usuwa wirtualny adres IP z usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="489cf-103">Deletes a virtual IP address from your Cloud Service.</span></span>

## <span data-ttu-id="489cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="489cf-104">SYNTAX</span></span>

```
Remove-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="489cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="489cf-105">DESCRIPTION</span></span>
<span data-ttu-id="489cf-106">Polecenie cmdlet **Remove-AzureVirtualIP** usuwa wirtualny adres IP (VIP) z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="489cf-106">The **Remove-AzureVirtualIP** cmdlet deletes a virtual IP (VIP) from an Azure service.</span></span>
<span data-ttu-id="489cf-107">Operacja kończy się powodzeniem tylko wtedy, gdy wirtualny adres IP nie ma skojarzonych z nim punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="489cf-107">The operation succeeds only if the virtual IP has no endpoints associated with it.</span></span>

## <span data-ttu-id="489cf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="489cf-108">EXAMPLES</span></span>

### <span data-ttu-id="489cf-109">Przykład 1: usuwanie wirtualnego adresu IP z usługi</span><span class="sxs-lookup"><span data-stu-id="489cf-109">Example 1: Remove a virtual IP address from a service</span></span>
```
PS C:\> Remove-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
```

<span data-ttu-id="489cf-110">To polecenie usuwa wirtualny adres IP z usługi.</span><span class="sxs-lookup"><span data-stu-id="489cf-110">This command removes a virtual IP address from a service.</span></span>

## <span data-ttu-id="489cf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="489cf-111">PARAMETERS</span></span>

### <span data-ttu-id="489cf-112">-Force</span><span class="sxs-lookup"><span data-stu-id="489cf-112">-Force</span></span>
<span data-ttu-id="489cf-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="489cf-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="489cf-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="489cf-114">-InformationAction</span></span>
<span data-ttu-id="489cf-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="489cf-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="489cf-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="489cf-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="489cf-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="489cf-117">Continue</span></span>
- <span data-ttu-id="489cf-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="489cf-118">Ignore</span></span>
- <span data-ttu-id="489cf-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="489cf-119">Inquire</span></span>
- <span data-ttu-id="489cf-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="489cf-120">SilentlyContinue</span></span>
- <span data-ttu-id="489cf-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="489cf-121">Stop</span></span>
- <span data-ttu-id="489cf-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="489cf-122">Suspend</span></span>

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

### <span data-ttu-id="489cf-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="489cf-123">-InformationVariable</span></span>
<span data-ttu-id="489cf-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="489cf-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="489cf-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="489cf-125">-Profile</span></span>
<span data-ttu-id="489cf-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="489cf-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="489cf-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="489cf-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="489cf-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="489cf-128">-ServiceName</span></span>
<span data-ttu-id="489cf-129">Określa nazwę usługi, z której ma zostać usunięty wirtualny adres IP.</span><span class="sxs-lookup"><span data-stu-id="489cf-129">Specifies the name of the service from which to remove a virtual IP address.</span></span>

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

### <span data-ttu-id="489cf-130">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="489cf-130">-VirtualIPName</span></span>
<span data-ttu-id="489cf-131">Określa nazwę wirtualnego adresu IP, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="489cf-131">Specifies the name of the virtual IP address to remove.</span></span>

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

### <span data-ttu-id="489cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489cf-132">CommonParameters</span></span>
<span data-ttu-id="489cf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="489cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489cf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="489cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489cf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="489cf-135">INPUTS</span></span>

## <span data-ttu-id="489cf-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="489cf-136">OUTPUTS</span></span>

### <span data-ttu-id="489cf-137">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="489cf-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="489cf-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="489cf-138">NOTES</span></span>

## <span data-ttu-id="489cf-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="489cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="489cf-140">Dodaj-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="489cf-140">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)


