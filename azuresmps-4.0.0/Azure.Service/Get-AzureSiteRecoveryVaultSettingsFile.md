---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055530"
---
# <span data-ttu-id="2b781-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2b781-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="2b781-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b781-102">SYNOPSIS</span></span>
<span data-ttu-id="2b781-103">Pobiera plik ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2b781-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="2b781-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b781-104">SYNTAX</span></span>

### <span data-ttu-id="2b781-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2b781-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b781-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2b781-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b781-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2b781-107">DESCRIPTION</span></span>
<span data-ttu-id="2b781-108">Polecenie cmdlet **Get-AzureSiteRecoveryVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2b781-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2b781-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b781-109">EXAMPLES</span></span>

### <span data-ttu-id="2b781-110">Przykład 1: uzyskiwanie pliku ustawień dla magazynu</span><span class="sxs-lookup"><span data-stu-id="2b781-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="2b781-111">Pierwsze polecenie pobiera aktywny magazyn usługi Azure Site Recovery o nazwie ContosoVault, używając polecenia cmdlet **Get-AzureSiteRecoveryVault** .</span><span class="sxs-lookup"><span data-stu-id="2b781-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="2b781-112">Polecenie zapisuje ten magazyn w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="2b781-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="2b781-113">Drugie polecenie pobiera plik ustawień dla magazynu przechowywanego w $Vault.</span><span class="sxs-lookup"><span data-stu-id="2b781-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="2b781-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b781-114">PARAMETERS</span></span>

### <span data-ttu-id="2b781-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2b781-115">-Location</span></span>
<span data-ttu-id="2b781-116">Określa lokalizację geograficzną, do której należy magazyn.</span><span class="sxs-lookup"><span data-stu-id="2b781-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2b781-117">-Name</span></span>
<span data-ttu-id="2b781-118">Określa nazwę magazynu.</span><span class="sxs-lookup"><span data-stu-id="2b781-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-119">-Path</span><span class="sxs-lookup"><span data-stu-id="2b781-119">-Path</span></span>
<span data-ttu-id="2b781-120">Określa ścieżkę pliku ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2b781-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="2b781-121">Aby zapisać ten plik lokalnie, Pobierz go z portalu magazynu odzyskiwania witryny po zakończeniu działania tego polecenia.</span><span class="sxs-lookup"><span data-stu-id="2b781-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b781-122">-Profile</span></span>
<span data-ttu-id="2b781-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b781-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b781-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2b781-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b781-125">-Site</span><span class="sxs-lookup"><span data-stu-id="2b781-125">-Site</span></span>
<span data-ttu-id="2b781-126">Określa witrynę, dla której ma zostać wyświetlony plik ustawień.</span><span class="sxs-lookup"><span data-stu-id="2b781-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="2b781-127">Aby uzyskać obiekt **witryny** , użyj polecenia cmdlet **Get-AzureSiteRecoverySite** .</span><span class="sxs-lookup"><span data-stu-id="2b781-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-128">-Identyfikator witryny</span><span class="sxs-lookup"><span data-stu-id="2b781-128">-SiteId</span></span>
<span data-ttu-id="2b781-129">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="2b781-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-130">-Sitename</span><span class="sxs-lookup"><span data-stu-id="2b781-130">-SiteName</span></span>
<span data-ttu-id="2b781-131">Określa nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="2b781-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-132">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="2b781-132">-Vault</span></span>
<span data-ttu-id="2b781-133">Określa magazyn witryny.</span><span class="sxs-lookup"><span data-stu-id="2b781-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b781-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b781-134">CommonParameters</span></span>
<span data-ttu-id="2b781-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b781-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b781-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b781-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b781-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b781-137">INPUTS</span></span>

## <span data-ttu-id="2b781-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b781-138">OUTPUTS</span></span>

## <span data-ttu-id="2b781-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b781-139">NOTES</span></span>

## <span data-ttu-id="2b781-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b781-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b781-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="2b781-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="2b781-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="2b781-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="2b781-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2b781-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="2b781-144">Import — AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2b781-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


