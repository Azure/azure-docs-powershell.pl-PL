---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007674"
---
# <span data-ttu-id="83d47-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="83d47-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="83d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d47-102">SYNOPSIS</span></span>
<span data-ttu-id="83d47-103">Importuje określony plik ustawień magazynu asr, aby ustawić kontekst magazynu (kontekst sesji programu PowerShell) dla kolejnych operacji ASR w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83d47-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="83d47-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83d47-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d47-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="83d47-105">DESCRIPTION</span></span>
<span data-ttu-id="83d47-106">Polecenie **cmdlet Import-AzRecoveryServicesAsrVaultSettingsFile** importuje plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="83d47-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="83d47-107">Plik ustawień magazynu służy do ustawienia kontekstu magazynu dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="83d47-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="83d47-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83d47-108">EXAMPLES</span></span>

### <span data-ttu-id="83d47-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83d47-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="83d47-110">Importowanie pliku ustawień określonego magazynu usług odzyskiwania i zwraca ustawienia importowanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="83d47-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="83d47-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d47-111">PARAMETERS</span></span>

### <span data-ttu-id="83d47-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d47-112">-DefaultProfile</span></span>
<span data-ttu-id="83d47-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83d47-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="83d47-114">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="83d47-114">-Path</span></span>
<span data-ttu-id="83d47-115">Określa ścieżkę folderu pliku ustawień magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="83d47-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="83d47-116">Ten plik można pobrać z portalu magazynu usług odzyskiwania i przechowywać lokalnie.</span><span class="sxs-lookup"><span data-stu-id="83d47-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="83d47-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83d47-117">-Confirm</span></span>
<span data-ttu-id="83d47-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83d47-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d47-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d47-119">-WhatIf</span></span>
<span data-ttu-id="83d47-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d47-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83d47-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83d47-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d47-122">CommonParameters</span></span>
<span data-ttu-id="83d47-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d47-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d47-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d47-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d47-125">INPUTS</span></span>

### <span data-ttu-id="83d47-126">System.String</span><span class="sxs-lookup"><span data-stu-id="83d47-126">System.String</span></span>

## <span data-ttu-id="83d47-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83d47-127">OUTPUTS</span></span>

### <span data-ttu-id="83d47-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="83d47-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="83d47-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83d47-129">NOTES</span></span>

## <span data-ttu-id="83d47-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83d47-130">RELATED LINKS</span></span>

[<span data-ttu-id="83d47-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="83d47-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
