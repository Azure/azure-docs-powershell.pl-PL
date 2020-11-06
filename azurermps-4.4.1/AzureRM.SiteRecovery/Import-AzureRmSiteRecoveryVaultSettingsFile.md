---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553091"
---
# <span data-ttu-id="2938b-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2938b-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="2938b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2938b-102">SYNOPSIS</span></span>
<span data-ttu-id="2938b-103">Importuje plik ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2938b-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2938b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2938b-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2938b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2938b-105">DESCRIPTION</span></span>
<span data-ttu-id="2938b-106">Polecenie cmdlet **Import-AzureRmSiteRecoveryVaultSettingsFile** umożliwia zaimportowanie pliku ustawień magazynu odzyskiwania witryny platformy Azure w celu ustawienia kontekstu magazynu dla kolejnych operacji odzyskiwania witryny w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="2938b-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="2938b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2938b-107">EXAMPLES</span></span>

## <span data-ttu-id="2938b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2938b-108">PARAMETERS</span></span>

### <span data-ttu-id="2938b-109">-Path</span><span class="sxs-lookup"><span data-stu-id="2938b-109">-Path</span></span>
<span data-ttu-id="2938b-110">Określa ścieżkę pliku ustawień magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="2938b-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="2938b-111">Ten plik można pobrać z portalu magazynu odzyskiwania witryny i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="2938b-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2938b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2938b-112">-DefaultProfile</span></span>
<span data-ttu-id="2938b-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2938b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2938b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2938b-114">CommonParameters</span></span>
<span data-ttu-id="2938b-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2938b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2938b-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2938b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2938b-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2938b-117">INPUTS</span></span>

## <span data-ttu-id="2938b-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2938b-118">OUTPUTS</span></span>

### <span data-ttu-id="2938b-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2938b-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2938b-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2938b-120">NOTES</span></span>

## <span data-ttu-id="2938b-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2938b-121">RELATED LINKS</span></span>

[<span data-ttu-id="2938b-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2938b-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
