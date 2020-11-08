---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 761317FE-55FD-4DCC-B997-4F27D041470F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77f58c4f3ee1c440e35c43648f92d21793efddc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055111"
---
# <span data-ttu-id="3fcdb-101">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3fcdb-101">Remove-AzureReservedIP</span></span>

## <span data-ttu-id="3fcdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3fcdb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcdb-103">Usuwa zastrzeżony adres IP według jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-103">Removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3fcdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3fcdb-104">SYNTAX</span></span>

```
Remove-AzureReservedIP [-ReservedIPName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3fcdb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3fcdb-105">DESCRIPTION</span></span>
<span data-ttu-id="3fcdb-106">Polecenie cmdlet **Remove-AzureReservedIP** usuwa zastrzeżony adres IP według jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-106">The **Remove-AzureReservedIP** cmdlet removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3fcdb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3fcdb-107">EXAMPLES</span></span>

### <span data-ttu-id="3fcdb-108">Przykład 1: usuwanie zastrzeżonego adresu IP według jego nazwy</span><span class="sxs-lookup"><span data-stu-id="3fcdb-108">Example 1: Remove a reserved IP address by its name</span></span>
```
PS C:\> Remove-AzureReservedIP -ReservedIPName $name
```

<span data-ttu-id="3fcdb-109">To polecenie usuwa zastrzeżony adres IP według jego nazwy.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-109">This command removes a reserved IP address by its name.</span></span>

## <span data-ttu-id="3fcdb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3fcdb-110">PARAMETERS</span></span>

### <span data-ttu-id="3fcdb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3fcdb-111">-Force</span></span>
<span data-ttu-id="3fcdb-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3fcdb-113">-InformationAction</span></span>
<span data-ttu-id="3fcdb-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3fcdb-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3fcdb-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3fcdb-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="3fcdb-116">Continue</span></span>
- <span data-ttu-id="3fcdb-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="3fcdb-117">Ignore</span></span>
- <span data-ttu-id="3fcdb-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="3fcdb-118">Inquire</span></span>
- <span data-ttu-id="3fcdb-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3fcdb-119">SilentlyContinue</span></span>
- <span data-ttu-id="3fcdb-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="3fcdb-120">Stop</span></span>
- <span data-ttu-id="3fcdb-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="3fcdb-121">Suspend</span></span>

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

### <span data-ttu-id="3fcdb-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3fcdb-122">-InformationVariable</span></span>
<span data-ttu-id="3fcdb-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3fcdb-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="3fcdb-124">-Profile</span></span>
<span data-ttu-id="3fcdb-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3fcdb-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3fcdb-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="3fcdb-127">-ReservedIPName</span></span>
<span data-ttu-id="3fcdb-128">Określa nazwę zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-128">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcdb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcdb-129">CommonParameters</span></span>
<span data-ttu-id="3fcdb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fcdb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcdb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fcdb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcdb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3fcdb-132">INPUTS</span></span>

## <span data-ttu-id="3fcdb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3fcdb-133">OUTPUTS</span></span>

## <span data-ttu-id="3fcdb-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3fcdb-134">NOTES</span></span>

## <span data-ttu-id="3fcdb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3fcdb-135">RELATED LINKS</span></span>

[<span data-ttu-id="3fcdb-136">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3fcdb-136">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="3fcdb-137">Nowe — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3fcdb-137">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="3fcdb-138">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="3fcdb-138">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


