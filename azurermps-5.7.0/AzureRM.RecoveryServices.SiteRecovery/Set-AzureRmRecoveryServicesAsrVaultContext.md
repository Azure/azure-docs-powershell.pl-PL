---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544192"
---
# <span data-ttu-id="d559b-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="d559b-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="d559b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d559b-102">SYNOPSIS</span></span>
<span data-ttu-id="d559b-103">Umożliwia ustawienie kontekstu magazynu usług odzyskiwania, który ma być stosowany do kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d559b-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d559b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d559b-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d559b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d559b-105">DESCRIPTION</span></span>
<span data-ttu-id="d559b-106">Polecenie cmdlet **Set-AzureRmRecoveryServicesAsrVaultContext** ustawia kontekst magazynu usługi Azure Site Recovery dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="d559b-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="d559b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d559b-107">EXAMPLES</span></span>

### <span data-ttu-id="d559b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d559b-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="d559b-109">Ustawia kontekst magazynu dla określonego magazynu usług odzyskiwania dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d559b-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="d559b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d559b-110">PARAMETERS</span></span>

### <span data-ttu-id="d559b-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d559b-111">-Confirm</span></span>
<span data-ttu-id="d559b-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d559b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d559b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d559b-113">-DefaultProfile</span></span>
<span data-ttu-id="d559b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d559b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d559b-115">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="d559b-115">-Vault</span></span>
<span data-ttu-id="d559b-116">Obiekt magazynu usług Recovery Services odpowiadający magazynowi usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="d559b-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d559b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d559b-117">-WhatIf</span></span>
<span data-ttu-id="d559b-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d559b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d559b-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d559b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d559b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d559b-120">CommonParameters</span></span>
<span data-ttu-id="d559b-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d559b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d559b-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d559b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d559b-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d559b-123">INPUTS</span></span>

### <span data-ttu-id="d559b-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="d559b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="d559b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d559b-125">OUTPUTS</span></span>

### <span data-ttu-id="d559b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="d559b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="d559b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d559b-127">NOTES</span></span>

## <span data-ttu-id="d559b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d559b-128">RELATED LINKS</span></span>
