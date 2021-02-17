---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 68ae9b9ad54772ba4157e02ebe602f35b2b5fe64
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399791"
---
# <span data-ttu-id="31013-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="31013-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="31013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31013-102">SYNOPSIS</span></span>
<span data-ttu-id="31013-103">Importuje określony plik ustawień magazynu asr, aby ustawić kontekst magazynu (kontekst sesji programu PowerShell) dla kolejnych operacji ASR w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31013-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="31013-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="31013-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31013-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="31013-105">DESCRIPTION</span></span>
<span data-ttu-id="31013-106">Polecenie **cmdlet Import-AzRecoveryServicesAsrVaultSettingsFile** importuje plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="31013-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="31013-107">Plik ustawień magazynu służy do ustawienia kontekstu magazynu dla kolejnych operacji Azure Site Recovery w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="31013-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="31013-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="31013-108">EXAMPLES</span></span>

### <span data-ttu-id="31013-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31013-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="31013-110">Importowanie pliku ustawień określonego magazynu usług odzyskiwania i zwraca ustawienia importowanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="31013-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="31013-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31013-111">PARAMETERS</span></span>

### <span data-ttu-id="31013-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31013-112">-DefaultProfile</span></span>
<span data-ttu-id="31013-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="31013-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="31013-114">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="31013-114">-Path</span></span>
<span data-ttu-id="31013-115">Określa ścieżkę folderu pliku ustawień magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="31013-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="31013-116">Ten plik można pobrać z portalu magazynu usług odzyskiwania i przechowywać lokalnie.</span><span class="sxs-lookup"><span data-stu-id="31013-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="31013-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31013-117">-Confirm</span></span>
<span data-ttu-id="31013-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="31013-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31013-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31013-119">-WhatIf</span></span>
<span data-ttu-id="31013-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31013-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31013-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="31013-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31013-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31013-122">CommonParameters</span></span>
<span data-ttu-id="31013-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31013-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31013-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31013-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31013-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31013-125">INPUTS</span></span>

### <span data-ttu-id="31013-126">System.String</span><span class="sxs-lookup"><span data-stu-id="31013-126">System.String</span></span>

## <span data-ttu-id="31013-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31013-127">OUTPUTS</span></span>

### <span data-ttu-id="31013-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="31013-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="31013-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="31013-129">NOTES</span></span>

## <span data-ttu-id="31013-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31013-130">RELATED LINKS</span></span>

