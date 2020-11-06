---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552588"
---
# <span data-ttu-id="b0c21-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b0c21-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="b0c21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0c21-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c21-103">Pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0c21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0c21-104">SYNTAX</span></span>

### <span data-ttu-id="b0c21-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="b0c21-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0c21-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="b0c21-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0c21-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="b0c21-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c21-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b0c21-108">DESCRIPTION</span></span>
<span data-ttu-id="b0c21-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b0c21-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0c21-110">EXAMPLES</span></span>

### <span data-ttu-id="b0c21-111">Przykład 1: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="b0c21-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="b0c21-112">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="b0c21-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="b0c21-113">Drugie polecenie ustawia zmienną $CredsPath na C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="b0c21-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="b0c21-114">Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w $CredsPath usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c21-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="b0c21-115">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="b0c21-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="b0c21-116">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01 typu magazynu siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="b0c21-117">Przykład 3: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="b0c21-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="b0c21-118">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="b0c21-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="b0c21-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0c21-119">PARAMETERS</span></span>

### <span data-ttu-id="b0c21-120">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="b0c21-120">-Backup</span></span>
<span data-ttu-id="b0c21-121">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c21-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c21-122">-DefaultProfile</span></span>
<span data-ttu-id="b0c21-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0c21-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-124">-Path</span><span class="sxs-lookup"><span data-stu-id="b0c21-124">-Path</span></span>
<span data-ttu-id="b0c21-125">Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="b0c21-126">Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i zapisać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="b0c21-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b0c21-127">-SiteFriendlyName</span></span>
<span data-ttu-id="b0c21-128">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="b0c21-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="b0c21-129">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b0c21-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-130">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="b0c21-130">-SiteIdentifier</span></span>
<span data-ttu-id="b0c21-131">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="b0c21-131">Specifies the site identifier.</span></span>
<span data-ttu-id="b0c21-132">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="b0c21-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-133">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="b0c21-133">-SiteRecovery</span></span>
<span data-ttu-id="b0c21-134">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-135">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="b0c21-135">-Vault</span></span>
<span data-ttu-id="b0c21-136">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b0c21-136">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0c21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c21-137">CommonParameters</span></span>
<span data-ttu-id="b0c21-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0c21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c21-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c21-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c21-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0c21-140">INPUTS</span></span>

### <span data-ttu-id="b0c21-141">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b0c21-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="b0c21-142">Parametry: Magazyn (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0c21-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="b0c21-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0c21-143">OUTPUTS</span></span>

### <span data-ttu-id="b0c21-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="b0c21-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="b0c21-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0c21-145">NOTES</span></span>

## <span data-ttu-id="b0c21-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0c21-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0c21-147">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b0c21-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b0c21-148">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b0c21-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="b0c21-149">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b0c21-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


