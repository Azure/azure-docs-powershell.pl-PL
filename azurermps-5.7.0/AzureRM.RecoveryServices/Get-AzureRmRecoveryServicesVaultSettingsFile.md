---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: b272f22c0bac37f5318deff50f1f0b56a849ce2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718028"
---
# <span data-ttu-id="63fb6-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="63fb6-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="63fb6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="63fb6-103">Pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63fb6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63fb6-104">SYNTAX</span></span>

### <span data-ttu-id="63fb6-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="63fb6-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63fb6-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="63fb6-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63fb6-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="63fb6-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63fb6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="63fb6-108">DESCRIPTION</span></span>
<span data-ttu-id="63fb6-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="63fb6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63fb6-110">EXAMPLES</span></span>

### <span data-ttu-id="63fb6-111">Przykład 1: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="63fb6-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="63fb6-112">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="63fb6-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="63fb6-113">Drugie polecenie ustawia zmienną $CredsPath na C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="63fb6-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="63fb6-114">Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w $CredsPath usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="63fb6-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="63fb6-115">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="63fb6-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="63fb6-116">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01 typu magazynu siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="63fb6-117">Przykład 3: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="63fb6-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="63fb6-118">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="63fb6-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="63fb6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63fb6-119">PARAMETERS</span></span>

### <span data-ttu-id="63fb6-120">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="63fb6-120">-Backup</span></span>
<span data-ttu-id="63fb6-121">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="63fb6-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-122">-Path</span><span class="sxs-lookup"><span data-stu-id="63fb6-122">-Path</span></span>
<span data-ttu-id="63fb6-123">Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-123">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="63fb6-124">Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i zapisać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="63fb6-124">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-125">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="63fb6-125">-SiteFriendlyName</span></span>
<span data-ttu-id="63fb6-126">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="63fb6-126">Specifies the site friendly name.</span></span>
<span data-ttu-id="63fb6-127">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="63fb6-127">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-128">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="63fb6-128">-SiteIdentifier</span></span>
<span data-ttu-id="63fb6-129">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="63fb6-129">Specifies the site identifier.</span></span>
<span data-ttu-id="63fb6-130">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="63fb6-130">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-131">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="63fb6-131">-SiteRecovery</span></span>
<span data-ttu-id="63fb6-132">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-132">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-133">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="63fb6-133">-Vault</span></span>
<span data-ttu-id="63fb6-134">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63fb6-134">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fb6-135">-DefaultProfile</span></span>
<span data-ttu-id="63fb6-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63fb6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fb6-137">CommonParameters</span></span>
<span data-ttu-id="63fb6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fb6-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fb6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fb6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63fb6-140">INPUTS</span></span>

### <span data-ttu-id="63fb6-141">ARSVault</span><span class="sxs-lookup"><span data-stu-id="63fb6-141">ARSVault</span></span>
<span data-ttu-id="63fb6-142">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="63fb6-142">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="63fb6-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63fb6-143">OUTPUTS</span></span>

### <span data-ttu-id="63fb6-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="63fb6-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="63fb6-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63fb6-145">NOTES</span></span>

## <span data-ttu-id="63fb6-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63fb6-146">RELATED LINKS</span></span>

[<span data-ttu-id="63fb6-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="63fb6-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="63fb6-148">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="63fb6-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="63fb6-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="63fb6-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


