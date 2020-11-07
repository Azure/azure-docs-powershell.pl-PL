---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 9595E785-6DBF-433C-83B3-8506A3B49B13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 621e5ac05c5f975ff3878781bcb8c5a1b40c04bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718441"
---
# <span data-ttu-id="bc162-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bc162-101">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="bc162-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc162-102">SYNOPSIS</span></span>
<span data-ttu-id="bc162-103">Pobiera plik ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="bc162-103">Gets the Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc162-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc162-104">SYNTAX</span></span>

### <span data-ttu-id="bc162-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bc162-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc162-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="bc162-106">Default</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc162-107">ForSite</span><span class="sxs-lookup"><span data-stu-id="bc162-107">ForSite</span></span>
```
Get-AzureRmSiteRecoveryVaultSettingsFile -Vault <ASRVault> -SiteIdentifier <String> -SiteFriendlyName <String>
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc162-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bc162-108">DESCRIPTION</span></span>
<span data-ttu-id="bc162-109">Polecenie cmdlet **Get-AzureRmSiteRecoveryVaultSettingsFile** pobiera plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="bc162-109">The **Get-AzureRmSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="bc162-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc162-110">EXAMPLES</span></span>

## <span data-ttu-id="bc162-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc162-111">PARAMETERS</span></span>

### <span data-ttu-id="bc162-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc162-112">-DefaultProfile</span></span>
<span data-ttu-id="bc162-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bc162-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc162-114">-Path</span><span class="sxs-lookup"><span data-stu-id="bc162-114">-Path</span></span>
<span data-ttu-id="bc162-115">Określa ścieżkę do pliku ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="bc162-115">Specifies the path to the Site Recovery vault settings file.</span></span>
<span data-ttu-id="bc162-116">Aby zapisać ten plik lokalnie, Pobierz go z portalu magazynu odzyskiwania witryny po ukończeniu polecenia.</span><span class="sxs-lookup"><span data-stu-id="bc162-116">To store this file locally, download it from the Site Recovery vault portal once the command completes.</span></span>

```yaml
Type: String
Parameter Sets: Default, ForSite
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc162-117">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="bc162-117">-SiteFriendlyName</span></span>
<span data-ttu-id="bc162-118">Określa przyjazną nazwę magazynu witryny, gdy witryna jest witryną funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bc162-118">Specifies the site friendly name for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="bc162-119">-SiteIdentifier</span><span class="sxs-lookup"><span data-stu-id="bc162-119">-SiteIdentifier</span></span>
<span data-ttu-id="bc162-120">Określa identyfikator witryny dla magazynu, gdy witryna jest witryną funkcji Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bc162-120">Specifies the site identifier for the vault when the site is a Hyper-V site.</span></span>

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

### <span data-ttu-id="bc162-121">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="bc162-121">-Vault</span></span>
<span data-ttu-id="bc162-122">Określa obiekt magazynu dla witryny.</span><span class="sxs-lookup"><span data-stu-id="bc162-122">Specifies the vault object for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: Default, ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc162-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc162-123">CommonParameters</span></span>
<span data-ttu-id="bc162-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc162-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc162-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc162-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc162-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc162-126">INPUTS</span></span>

### <span data-ttu-id="bc162-127">ASRVault</span><span class="sxs-lookup"><span data-stu-id="bc162-127">ASRVault</span></span>
<span data-ttu-id="bc162-128">Parametr "magazyn" akceptuje wartość typu "ASRVault" z potoku.</span><span class="sxs-lookup"><span data-stu-id="bc162-128">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="bc162-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc162-129">OUTPUTS</span></span>

### <span data-ttu-id="bc162-130">Microsoft. Azure. Commands. SiteRecovery. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="bc162-130">Microsoft.Azure.Commands.SiteRecovery.VaultSettingsFilePath</span></span>

## <span data-ttu-id="bc162-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc162-131">NOTES</span></span>

## <span data-ttu-id="bc162-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc162-132">RELATED LINKS</span></span>

[<span data-ttu-id="bc162-133">Import — AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bc162-133">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureRmSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="bc162-134">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="bc162-134">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)
