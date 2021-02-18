---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 0d074c18ad9b5f9ea34a465acd4a91a88d4b69ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192922"
---
# <span data-ttu-id="d52e2-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d52e2-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="d52e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d52e2-102">SYNOPSIS</span></span>
<span data-ttu-id="d52e2-103">Pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d52e2-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="d52e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d52e2-104">SYNTAX</span></span>

### <span data-ttu-id="d52e2-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d52e2-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d52e2-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d52e2-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d52e2-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="d52e2-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d52e2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d52e2-108">DESCRIPTION</span></span>
<span data-ttu-id="d52e2-109">Polecenie **cmdlet Get-AzRecoveryServicesVaultSettingsFile** pobiera plik ustawień dla magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d52e2-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="d52e2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d52e2-110">EXAMPLES</span></span>

### <span data-ttu-id="d52e2-111">Przykład 1. Rejestrowanie komputera z systemem Windows Server lub dpm na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="d52e2-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="d52e2-112">Pierwsze polecenie pobiera magazyn o nazwie TestVault, a następnie przechowuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="d52e2-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="d52e2-113">Drugie polecenie ustawia zmienną $CredsPath C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="d52e2-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="d52e2-114">Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w usłudze $CredsPath dla usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d52e2-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="d52e2-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d52e2-115">Example 2</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d52e2-116">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01 typu magazynu siteRecovery.</span><span class="sxs-lookup"><span data-stu-id="d52e2-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="d52e2-117">Przykład 3. Rejestrowanie komputera z systemem Windows Server lub dpm na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="d52e2-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```powershell
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="d52e2-118">Polecenie pobiera plik poświadczeń magazynu dla $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="d52e2-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="d52e2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d52e2-119">PARAMETERS</span></span>

### <span data-ttu-id="d52e2-120">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="d52e2-120">-Backup</span></span>
<span data-ttu-id="d52e2-121">Wskazuje, że plik poświadczeń magazynu ma zastosowanie do usługi Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="d52e2-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="d52e2-122">— Certyfikat</span><span class="sxs-lookup"><span data-stu-id="d52e2-122">-Certificate</span></span>
<span data-ttu-id="d52e2-123">{{Fill Certificate Description}}</span><span class="sxs-lookup"><span data-stu-id="d52e2-123">{{Fill Certificate Description}}</span></span>

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

### <span data-ttu-id="d52e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52e2-124">-DefaultProfile</span></span>
<span data-ttu-id="d52e2-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d52e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d52e2-126">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d52e2-126">-Path</span></span>
<span data-ttu-id="d52e2-127">Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d52e2-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="d52e2-128">Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="d52e2-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="d52e2-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d52e2-129">-SiteFriendlyName</span></span>
<span data-ttu-id="d52e2-130">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="d52e2-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="d52e2-131">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d52e2-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="d52e2-132">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="d52e2-132">-SiteIdentifier</span></span>
<span data-ttu-id="d52e2-133">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="d52e2-133">Specifies the site identifier.</span></span>
<span data-ttu-id="d52e2-134">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d52e2-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="d52e2-135">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="d52e2-135">-SiteRecovery</span></span>
<span data-ttu-id="d52e2-136">Wskazuje, że plik poświadczeń magazynu ma zastosowanie do usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d52e2-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="d52e2-137">— magazyn</span><span class="sxs-lookup"><span data-stu-id="d52e2-137">-Vault</span></span>
<span data-ttu-id="d52e2-138">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d52e2-138">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="d52e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52e2-139">CommonParameters</span></span>
<span data-ttu-id="d52e2-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52e2-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d52e2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52e2-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52e2-142">INPUTS</span></span>

### <span data-ttu-id="d52e2-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="d52e2-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d52e2-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d52e2-144">OUTPUTS</span></span>

### <span data-ttu-id="d52e2-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="d52e2-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="d52e2-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d52e2-146">NOTES</span></span>

## <span data-ttu-id="d52e2-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d52e2-147">RELATED LINKS</span></span>

[<span data-ttu-id="d52e2-148">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d52e2-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="d52e2-149">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d52e2-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="d52e2-150">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d52e2-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


