---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526154"
---
# <span data-ttu-id="d8ca8-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d8ca8-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="d8ca8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ca8-103">Importowanie określonego pliku ustawień magazynu ASR w celu ustawienia kontekstu magazynu (kontekstu sesji programu PowerShell) dla kolejnych operacji ASR w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ca8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8ca8-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ca8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ca8-106">Polecenie cmdlet **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** importuje plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="d8ca8-107">Plik ustawienia magazynu służy do ustawiania kontekstu magazynu dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="d8ca8-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8ca8-108">EXAMPLES</span></span>

### <span data-ttu-id="d8ca8-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8ca8-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="d8ca8-110">Importuje określone pliki ustawień magazynu usług Recovery Services i zwraca ustawienia zaimportowanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="d8ca8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8ca8-111">PARAMETERS</span></span>

### <span data-ttu-id="d8ca8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ca8-112">-DefaultProfile</span></span>
<span data-ttu-id="d8ca8-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d8ca8-114">-Path</span><span class="sxs-lookup"><span data-stu-id="d8ca8-114">-Path</span></span>
<span data-ttu-id="d8ca8-115">Określa ścieżkę folderu ustawień magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="d8ca8-116">Ten plik można pobrać z portalu magazynu usług Recovery Services i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="d8ca8-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8ca8-117">-Confirm</span></span>
<span data-ttu-id="d8ca8-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ca8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ca8-119">-WhatIf</span></span>
<span data-ttu-id="d8ca8-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8ca8-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8ca8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ca8-122">CommonParameters</span></span>
<span data-ttu-id="d8ca8-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ca8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ca8-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ca8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ca8-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ca8-125">INPUTS</span></span>

### <span data-ttu-id="d8ca8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d8ca8-126">System.String</span></span>

## <span data-ttu-id="d8ca8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8ca8-127">OUTPUTS</span></span>

### <span data-ttu-id="d8ca8-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d8ca8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d8ca8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8ca8-129">NOTES</span></span>

## <span data-ttu-id="d8ca8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8ca8-130">RELATED LINKS</span></span>

[<span data-ttu-id="d8ca8-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d8ca8-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
