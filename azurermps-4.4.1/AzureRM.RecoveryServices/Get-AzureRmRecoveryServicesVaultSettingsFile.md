---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550808"
---
# <span data-ttu-id="f97de-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f97de-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="f97de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f97de-102">SYNOPSIS</span></span>
<span data-ttu-id="f97de-103">Pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f97de-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f97de-104">SYNTAX</span></span>

### <span data-ttu-id="f97de-105">ForSite</span><span class="sxs-lookup"><span data-stu-id="f97de-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f97de-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="f97de-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f97de-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="f97de-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f97de-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f97de-108">DESCRIPTION</span></span>
<span data-ttu-id="f97de-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f97de-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f97de-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f97de-110">EXAMPLES</span></span>

### <span data-ttu-id="f97de-111">Przykład 1: rejestrowanie kopii zapasowej systemu Windows Server lub programu DPM na platformie Azure Backup</span><span class="sxs-lookup"><span data-stu-id="f97de-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="f97de-112">Pierwsze polecenie uzyskuje magazyn o nazwie TestVault, a następnie zapisuje go w zmiennej $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="f97de-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="f97de-113">Drugie polecenie ustawia zmienną $CredsPath na C:\Downloads.</span><span class="sxs-lookup"><span data-stu-id="f97de-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>

<span data-ttu-id="f97de-114">Ostatnie polecenie pobiera plik poświadczeń magazynu dla $Vault 01 przy użyciu poświadczeń w $CredsPath usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="f97de-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

## <span data-ttu-id="f97de-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f97de-115">PARAMETERS</span></span>

### <span data-ttu-id="f97de-116">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="f97de-116">-Backup</span></span>
<span data-ttu-id="f97de-117">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Kopia zapasowa Azure.</span><span class="sxs-lookup"><span data-stu-id="f97de-117">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

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

### <span data-ttu-id="f97de-118">-Path</span><span class="sxs-lookup"><span data-stu-id="f97de-118">-Path</span></span>
<span data-ttu-id="f97de-119">Określa ścieżkę do pliku ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f97de-119">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="f97de-120">Możesz pobrać ten plik z portalu magazynu usługi Azure Site Recovery i zapisać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="f97de-120">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="f97de-121">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f97de-121">-SiteFriendlyName</span></span>
<span data-ttu-id="f97de-122">Określa przyjazną nazwę witryny.</span><span class="sxs-lookup"><span data-stu-id="f97de-122">Specifies the site friendly name.</span></span>
<span data-ttu-id="f97de-123">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f97de-123">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f97de-124">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="f97de-124">-SiteIdentifier</span></span>
<span data-ttu-id="f97de-125">Określa identyfikator witryny.</span><span class="sxs-lookup"><span data-stu-id="f97de-125">Specifies the site identifier.</span></span>
<span data-ttu-id="f97de-126">Użyj tego parametru, jeśli pobierasz poświadczenia magazynu dla witryny Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="f97de-126">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

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

### <span data-ttu-id="f97de-127">-SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f97de-127">-SiteRecovery</span></span>
<span data-ttu-id="f97de-128">Wskazuje, że plik poświadczeń magazynu dotyczy usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f97de-128">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

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

### <span data-ttu-id="f97de-129">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="f97de-129">-Vault</span></span>
<span data-ttu-id="f97de-130">Określa obiekt magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f97de-130">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="f97de-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97de-131">-DefaultProfile</span></span>
<span data-ttu-id="f97de-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f97de-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97de-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97de-133">CommonParameters</span></span>
<span data-ttu-id="f97de-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97de-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97de-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97de-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97de-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f97de-136">INPUTS</span></span>

### <span data-ttu-id="f97de-137">ARSVault</span><span class="sxs-lookup"><span data-stu-id="f97de-137">ARSVault</span></span>
<span data-ttu-id="f97de-138">Parametr "magazyn" akceptuje wartość typu "ARSVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="f97de-138">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="f97de-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f97de-139">OUTPUTS</span></span>

### <span data-ttu-id="f97de-140">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="f97de-140">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="f97de-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f97de-141">NOTES</span></span>

## <span data-ttu-id="f97de-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f97de-142">RELATED LINKS</span></span>

[<span data-ttu-id="f97de-143">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f97de-143">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="f97de-144">Nowe — AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f97de-144">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="f97de-145">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f97de-145">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


