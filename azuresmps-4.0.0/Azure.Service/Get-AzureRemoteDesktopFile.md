---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054586"
---
# <span data-ttu-id="d6f10-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="d6f10-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="d6f10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6f10-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f10-103">Pobiera plik RDP dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f10-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="d6f10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6f10-104">SYNTAX</span></span>

### <span data-ttu-id="d6f10-105">Pobierz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d6f10-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6f10-106">Wczesn</span><span class="sxs-lookup"><span data-stu-id="d6f10-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6f10-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6f10-107">DESCRIPTION</span></span>
<span data-ttu-id="d6f10-108">Polecenie cmdlet **Get-AzureRemoteDesktopFile** pobiera i zapisuje plik Podłączanie pulpitu zdalnego (RDP) dla maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d6f10-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="d6f10-109">Polecenie cmdlet może uruchomić połączenie pulpitu zdalnego z określoną maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="d6f10-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="d6f10-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6f10-110">EXAMPLES</span></span>

### <span data-ttu-id="d6f10-111">Przykład 1: uzyskiwanie pliku RDP</span><span class="sxs-lookup"><span data-stu-id="d6f10-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="d6f10-112">To polecenie pobiera plik RDP dla maszyny wirtualnej VirtualMachine07 o nazwie VirtualMachine07 działającej w usłudze o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="d6f10-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="d6f10-113">Polecenie zapisuje ten plik jako C:\temp\VirtualMachine07.rdp.</span><span class="sxs-lookup"><span data-stu-id="d6f10-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="d6f10-114">Przykład 2: Rozpoczynanie sesji zdalnej</span><span class="sxs-lookup"><span data-stu-id="d6f10-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="d6f10-115">To polecenie pobiera plik RDP dla maszyny wirtualnej VirtualMachine07 o nazwie VirtualMachine07 działającej w usłudze o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="d6f10-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="d6f10-116">Polecenie uruchamia sesję pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="d6f10-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="d6f10-117">Polecenie usuwa plik RDP po zamknięciu połączenia.</span><span class="sxs-lookup"><span data-stu-id="d6f10-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="d6f10-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6f10-118">PARAMETERS</span></span>

### <span data-ttu-id="d6f10-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d6f10-119">-InformationAction</span></span>
<span data-ttu-id="d6f10-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d6f10-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d6f10-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d6f10-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6f10-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d6f10-122">Continue</span></span>
- <span data-ttu-id="d6f10-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d6f10-123">Ignore</span></span>
- <span data-ttu-id="d6f10-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="d6f10-124">Inquire</span></span>
- <span data-ttu-id="d6f10-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d6f10-125">SilentlyContinue</span></span>
- <span data-ttu-id="d6f10-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d6f10-126">Stop</span></span>
- <span data-ttu-id="d6f10-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d6f10-127">Suspend</span></span>

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

### <span data-ttu-id="d6f10-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d6f10-128">-InformationVariable</span></span>
<span data-ttu-id="d6f10-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d6f10-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d6f10-130">-Uruchom</span><span class="sxs-lookup"><span data-stu-id="d6f10-130">-Launch</span></span>
<span data-ttu-id="d6f10-131">Wskazuje, że to polecenie cmdlet rozpoczyna sesję pulpitu zdalnego na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d6f10-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="d6f10-132">-LocalPath</span></span>
<span data-ttu-id="d6f10-133">Określa pełną ścieżkę pobranego pliku RDP na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="d6f10-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6f10-134">-Name</span></span>
<span data-ttu-id="d6f10-135">Umożliwia określenie maszyny wirtualnej, dla której to polecenie cmdlet pobiera plik RDP.</span><span class="sxs-lookup"><span data-stu-id="d6f10-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f10-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6f10-136">-Profile</span></span>
<span data-ttu-id="d6f10-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6f10-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6f10-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d6f10-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6f10-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d6f10-139">-ServiceName</span></span>
<span data-ttu-id="d6f10-140">Określa nazwę usługi platformy Azure, do której należy maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="d6f10-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="d6f10-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f10-141">CommonParameters</span></span>
<span data-ttu-id="d6f10-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6f10-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f10-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f10-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f10-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6f10-144">INPUTS</span></span>

## <span data-ttu-id="d6f10-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6f10-145">OUTPUTS</span></span>

## <span data-ttu-id="d6f10-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6f10-146">NOTES</span></span>

## <span data-ttu-id="d6f10-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6f10-147">RELATED LINKS</span></span>

