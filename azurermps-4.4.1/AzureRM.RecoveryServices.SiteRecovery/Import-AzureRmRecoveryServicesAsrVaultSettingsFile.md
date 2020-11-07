---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716895"
---
# <span data-ttu-id="2dac4-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2dac4-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="2dac4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2dac4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dac4-103">Importowanie określonego pliku ustawień magazynu ASR w celu ustawienia kontekstu magazynu (kontekstu sesji programu PowerShell) dla kolejnych operacji ASR w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2dac4-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dac4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2dac4-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dac4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2dac4-105">DESCRIPTION</span></span>
<span data-ttu-id="2dac4-106">Polecenie cmdlet **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** importuje plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2dac4-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="2dac4-107">Plik ustawienia magazynu służy do ustawiania kontekstu magazynu dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="2dac4-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="2dac4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2dac4-108">EXAMPLES</span></span>

### <span data-ttu-id="2dac4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2dac4-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="2dac4-110">Importuje określone pliki ustawień magazynu usług Recovery Services i zwraca ustawienia zaimportowanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="2dac4-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="2dac4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2dac4-111">PARAMETERS</span></span>

### <span data-ttu-id="2dac4-112">-Path</span><span class="sxs-lookup"><span data-stu-id="2dac4-112">-Path</span></span>
<span data-ttu-id="2dac4-113">Określa ścieżkę pliku ustawień magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="2dac4-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="2dac4-114">Ten plik można pobrać z portalu magazynu usług Recovery Services i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="2dac4-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="2dac4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dac4-115">-Confirm</span></span>
<span data-ttu-id="2dac4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dac4-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dac4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dac4-117">-WhatIf</span></span>
<span data-ttu-id="2dac4-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dac4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dac4-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2dac4-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dac4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dac4-120">CommonParameters</span></span>
<span data-ttu-id="2dac4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dac4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dac4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dac4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dac4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dac4-123">INPUTS</span></span>

### <span data-ttu-id="2dac4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2dac4-124">System.String</span></span>

## <span data-ttu-id="2dac4-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2dac4-125">OUTPUTS</span></span>

### <span data-ttu-id="2dac4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2dac4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2dac4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2dac4-127">NOTES</span></span>

## <span data-ttu-id="2dac4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dac4-128">RELATED LINKS</span></span>

[<span data-ttu-id="2dac4-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2dac4-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
