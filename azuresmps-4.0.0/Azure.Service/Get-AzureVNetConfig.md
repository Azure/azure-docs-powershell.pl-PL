---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055254"
---
# <span data-ttu-id="12d44-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="12d44-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="12d44-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12d44-102">SYNOPSIS</span></span>
<span data-ttu-id="12d44-103">Pobiera konfigurację sieci wirtualnej platformy Azure z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="12d44-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="12d44-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12d44-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="12d44-105">Opis</span><span class="sxs-lookup"><span data-stu-id="12d44-105">DESCRIPTION</span></span>
<span data-ttu-id="12d44-106">Polecenie cmdlet **Get-AzureVNetConfig** Pobiera konfigurację sieci wirtualnej bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="12d44-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="12d44-107">Jeśli określono parametr *ExportToFile* , zostanie utworzony plik konfiguracji sieci.</span><span class="sxs-lookup"><span data-stu-id="12d44-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="12d44-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12d44-108">EXAMPLES</span></span>

### <span data-ttu-id="12d44-109">Przykład 1: Pobieranie konfiguracji sieci wirtualnej bieżącej subskrypcji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="12d44-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="12d44-110">To polecenie pobiera konfigurację sieci wirtualnej bieżącej subskrypcji platformy Azure i wyświetla ją.</span><span class="sxs-lookup"><span data-stu-id="12d44-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="12d44-111">Przykład 2: pobranie konfiguracji sieci wirtualnej bieżącej subskrypcji platformy Azure i zapisanie jej w pliku lokalnym</span><span class="sxs-lookup"><span data-stu-id="12d44-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="12d44-112">To polecenie pobiera konfigurację sieci wirtualnej bieżącej subskrypcji platformy Azure, a następnie zapisuje ją w pliku lokalnym.</span><span class="sxs-lookup"><span data-stu-id="12d44-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="12d44-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12d44-113">PARAMETERS</span></span>

### <span data-ttu-id="12d44-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="12d44-114">-ExportToFile</span></span>
<span data-ttu-id="12d44-115">Określa ścieżkę i nazwę pliku konfiguracji sieci, który ma zostać utworzony na podstawie ustawień.</span><span class="sxs-lookup"><span data-stu-id="12d44-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12d44-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="12d44-116">-InformationAction</span></span>
<span data-ttu-id="12d44-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="12d44-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="12d44-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="12d44-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12d44-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="12d44-119">Continue</span></span>
- <span data-ttu-id="12d44-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="12d44-120">Ignore</span></span>
- <span data-ttu-id="12d44-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="12d44-121">Inquire</span></span>
- <span data-ttu-id="12d44-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="12d44-122">SilentlyContinue</span></span>
- <span data-ttu-id="12d44-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="12d44-123">Stop</span></span>
- <span data-ttu-id="12d44-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="12d44-124">Suspend</span></span>

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

### <span data-ttu-id="12d44-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="12d44-125">-InformationVariable</span></span>
<span data-ttu-id="12d44-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="12d44-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="12d44-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="12d44-127">-Profile</span></span>
<span data-ttu-id="12d44-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12d44-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="12d44-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="12d44-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="12d44-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d44-130">CommonParameters</span></span>
<span data-ttu-id="12d44-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12d44-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d44-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d44-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d44-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12d44-133">INPUTS</span></span>

## <span data-ttu-id="12d44-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12d44-134">OUTPUTS</span></span>

## <span data-ttu-id="12d44-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12d44-135">NOTES</span></span>

## <span data-ttu-id="12d44-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12d44-136">RELATED LINKS</span></span>

[<span data-ttu-id="12d44-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="12d44-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="12d44-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="12d44-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="12d44-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="12d44-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


