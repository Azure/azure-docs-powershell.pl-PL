---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: de3604a4bf1f9c46bf88b2f3cda25982672e9096
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053678"
---
# <span data-ttu-id="0cf11-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0cf11-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="0cf11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cf11-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf11-103">Importowanie określonego pliku ustawień magazynu ASR w celu ustawienia kontekstu magazynu (kontekstu sesji programu PowerShell) dla kolejnych operacji ASR w sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0cf11-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="0cf11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cf11-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0cf11-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf11-106">Polecenie cmdlet **Import-AzRecoveryServicesAsrVaultSettingsFile** importuje plik ustawień magazynu usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0cf11-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="0cf11-107">Plik ustawienia magazynu służy do ustawiania kontekstu magazynu dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="0cf11-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="0cf11-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cf11-108">EXAMPLES</span></span>

### <span data-ttu-id="0cf11-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0cf11-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="0cf11-110">Importuje określone pliki ustawień magazynu usług Recovery Services i zwraca ustawienia zaimportowanego magazynu.</span><span class="sxs-lookup"><span data-stu-id="0cf11-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="0cf11-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cf11-111">PARAMETERS</span></span>

### <span data-ttu-id="0cf11-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf11-112">-DefaultProfile</span></span>
<span data-ttu-id="0cf11-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cf11-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0cf11-114">-Path</span><span class="sxs-lookup"><span data-stu-id="0cf11-114">-Path</span></span>
<span data-ttu-id="0cf11-115">Określa ścieżkę folderu ustawień magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="0cf11-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="0cf11-116">Ten plik można pobrać z portalu magazynu usług Recovery Services i przechowywać go lokalnie.</span><span class="sxs-lookup"><span data-stu-id="0cf11-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="0cf11-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cf11-117">-Confirm</span></span>
<span data-ttu-id="0cf11-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf11-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf11-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf11-119">-WhatIf</span></span>
<span data-ttu-id="0cf11-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cf11-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cf11-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0cf11-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf11-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf11-122">CommonParameters</span></span>
<span data-ttu-id="0cf11-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf11-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf11-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cf11-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf11-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cf11-125">INPUTS</span></span>

### <span data-ttu-id="0cf11-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0cf11-126">System.String</span></span>

## <span data-ttu-id="0cf11-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cf11-127">OUTPUTS</span></span>

### <span data-ttu-id="0cf11-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0cf11-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0cf11-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cf11-129">NOTES</span></span>

## <span data-ttu-id="0cf11-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cf11-130">RELATED LINKS</span></span>

[<span data-ttu-id="0cf11-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0cf11-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
