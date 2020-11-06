---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551536"
---
# <span data-ttu-id="d5fe9-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d5fe9-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="d5fe9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fe9-103">Importuje plik ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5fe9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5fe9-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5fe9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fe9-106">Polecenie cmdlet **Import-AzureRmSiteRecoveryVaultSettingsFile** umożliwia zaimportowanie pliku ustawień magazynu odzyskiwania witryny platformy Azure w celu ustawienia kontekstu magazynu dla kolejnych operacji odzyskiwania witryny w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="d5fe9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5fe9-107">EXAMPLES</span></span>

## <span data-ttu-id="d5fe9-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5fe9-108">PARAMETERS</span></span>

### <span data-ttu-id="d5fe9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fe9-109">-DefaultProfile</span></span>
<span data-ttu-id="d5fe9-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fe9-111">-Path</span><span class="sxs-lookup"><span data-stu-id="d5fe9-111">-Path</span></span>
<span data-ttu-id="d5fe9-112">Określa ścieżkę pliku ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="d5fe9-113">Ten plik można pobrać z portalu magazynu odzyskiwania witryny i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="d5fe9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fe9-114">CommonParameters</span></span>
<span data-ttu-id="d5fe9-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fe9-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fe9-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fe9-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5fe9-117">INPUTS</span></span>

### <span data-ttu-id="d5fe9-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d5fe9-118">None</span></span>
<span data-ttu-id="d5fe9-119">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d5fe9-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5fe9-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5fe9-120">OUTPUTS</span></span>

### <span data-ttu-id="d5fe9-121">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d5fe9-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d5fe9-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5fe9-122">NOTES</span></span>

## <span data-ttu-id="d5fe9-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5fe9-123">RELATED LINKS</span></span>

[<span data-ttu-id="d5fe9-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d5fe9-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
