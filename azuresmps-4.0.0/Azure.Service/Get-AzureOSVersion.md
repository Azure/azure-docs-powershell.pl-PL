---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054603"
---
# <span data-ttu-id="43a97-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="43a97-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="43a97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43a97-102">SYNOPSIS</span></span>
<span data-ttu-id="43a97-103">Lista wszystkich systemów operacyjnych gościa platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43a97-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="43a97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43a97-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43a97-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43a97-105">DESCRIPTION</span></span>
<span data-ttu-id="43a97-106">Polecenie cmdlet **Get-AzureOSVersion** zawiera listę wszystkich dostępnych systemów operacyjnych gościa platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="43a97-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="43a97-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43a97-107">EXAMPLES</span></span>

### <span data-ttu-id="43a97-108">Przykład 1. Uzyskaj wszystkie dostępne systemy operacyjne</span><span class="sxs-lookup"><span data-stu-id="43a97-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="43a97-109">To polecenie pobiera obiekt zawierający listę wszystkich wersji systemów operacyjnych gościa, które są dostępne w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="43a97-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="43a97-110">Przykład 2: wyświetlanie informacji o systemie operacyjnym w tabeli</span><span class="sxs-lookup"><span data-stu-id="43a97-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="43a97-111">To polecenie pobiera obiekt zawierający listę wszystkich wersji systemów operacyjnych gościa, które są dostępne w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="43a97-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="43a97-112">Polecenie przekazuje je do polecenia cmdlet **Format-Table** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="43a97-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43a97-113">Ten aplet polecenia sformatuje je jako tabelę przedstawiającą rodzinę systemów operacyjnych, etykietę rodziny systemów operacyjnych i wersję.</span><span class="sxs-lookup"><span data-stu-id="43a97-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="43a97-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43a97-114">PARAMETERS</span></span>

### <span data-ttu-id="43a97-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43a97-115">-InformationAction</span></span>
<span data-ttu-id="43a97-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="43a97-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43a97-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="43a97-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43a97-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="43a97-118">Continue</span></span>
- <span data-ttu-id="43a97-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="43a97-119">Ignore</span></span>
- <span data-ttu-id="43a97-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="43a97-120">Inquire</span></span>
- <span data-ttu-id="43a97-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43a97-121">SilentlyContinue</span></span>
- <span data-ttu-id="43a97-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="43a97-122">Stop</span></span>
- <span data-ttu-id="43a97-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="43a97-123">Suspend</span></span>

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

### <span data-ttu-id="43a97-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43a97-124">-InformationVariable</span></span>
<span data-ttu-id="43a97-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="43a97-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43a97-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="43a97-126">-Profile</span></span>
<span data-ttu-id="43a97-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43a97-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43a97-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="43a97-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43a97-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a97-129">CommonParameters</span></span>
<span data-ttu-id="43a97-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43a97-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a97-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43a97-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a97-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43a97-132">INPUTS</span></span>

## <span data-ttu-id="43a97-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43a97-133">OUTPUTS</span></span>

## <span data-ttu-id="43a97-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43a97-134">NOTES</span></span>

## <span data-ttu-id="43a97-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43a97-135">RELATED LINKS</span></span>

[<span data-ttu-id="43a97-136">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="43a97-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


