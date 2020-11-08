---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232951"
---
# <span data-ttu-id="87d5c-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="87d5c-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="87d5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="87d5c-103">Pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="87d5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87d5c-104">SYNTAX</span></span>

### <span data-ttu-id="87d5c-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="87d5c-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87d5c-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="87d5c-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87d5c-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="87d5c-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d5c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87d5c-108">DESCRIPTION</span></span>
<span data-ttu-id="87d5c-109">Polecenie cmdlet **Get-AzRecoveryServicesVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="87d5c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87d5c-110">EXAMPLES</span></span>

### <span data-ttu-id="87d5c-111">Przykład 1: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="87d5c-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="87d5c-112">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="87d5c-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="87d5c-113">Drugie polecenie ustawia zmienną $CredsPath na C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="87d5c-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="87d5c-114">Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w $CredsPath usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="87d5c-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="87d5c-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="87d5c-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="87d5c-116">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01 typu magazynu siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="87d5c-117">Przykład 3: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="87d5c-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="87d5c-118">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="87d5c-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="87d5c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87d5c-119">PARAMETERS</span></span>

### <span data-ttu-id="87d5c-120">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="87d5c-120">-Backup</span></span>
<span data-ttu-id="87d5c-121">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="87d5c-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-122">-Certificate</span><span class="sxs-lookup"><span data-stu-id="87d5c-122">-Certificate</span></span>
<span data-ttu-id="87d5c-123">{{Opis certyfikatu do wypełniania}}</span><span class="sxs-lookup"><span data-stu-id="87d5c-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d5c-124">-DefaultProfile</span></span>
<span data-ttu-id="87d5c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87d5c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-126">-Path</span><span class="sxs-lookup"><span data-stu-id="87d5c-126">-Path</span></span>
<span data-ttu-id="87d5c-127">Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="87d5c-128">Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i zapisać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="87d5c-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="87d5c-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="87d5c-129">-SiteFriendlyName</span></span>
<span data-ttu-id="87d5c-130">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="87d5c-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="87d5c-131">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="87d5c-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="87d5c-132">-SiteIdentifier</span></span>
<span data-ttu-id="87d5c-133">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="87d5c-133">Specifies the site identifier.</span></span>
<span data-ttu-id="87d5c-134">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="87d5c-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="87d5c-135">-SiteRecovery</span></span>
<span data-ttu-id="87d5c-136">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87d5c-137">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="87d5c-137">-Vault</span></span>
<span data-ttu-id="87d5c-138">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87d5c-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="87d5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d5c-139">CommonParameters</span></span>
<span data-ttu-id="87d5c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d5c-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87d5c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d5c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87d5c-142">INPUTS</span></span>

### <span data-ttu-id="87d5c-143">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="87d5c-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="87d5c-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87d5c-144">OUTPUTS</span></span>

### <span data-ttu-id="87d5c-145">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="87d5c-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="87d5c-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87d5c-146">NOTES</span></span>

## <span data-ttu-id="87d5c-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87d5c-147">RELATED LINKS</span></span>

[<span data-ttu-id="87d5c-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="87d5c-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="87d5c-149">Nowe — AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="87d5c-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="87d5c-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="87d5c-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


