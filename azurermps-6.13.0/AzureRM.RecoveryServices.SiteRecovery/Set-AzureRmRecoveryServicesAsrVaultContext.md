---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526134"
---
# <span data-ttu-id="b23d1-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b23d1-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b23d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b23d1-102">SYNOPSIS</span></span>
<span data-ttu-id="b23d1-103">Umożliwia ustawienie kontekstu magazynu usług odzyskiwania, który ma być stosowany do kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b23d1-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b23d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b23d1-104">SYNTAX</span></span>

### <span data-ttu-id="b23d1-105">AzureRecoveryServicesVault (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b23d1-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b23d1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b23d1-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b23d1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b23d1-107">DESCRIPTION</span></span>
<span data-ttu-id="b23d1-108">Polecenie cmdlet **Set-AzureRmRecoveryServicesAsrVaultContext** ustawia kontekst magazynu usługi Azure Site Recovery dla kolejnych operacji.</span><span class="sxs-lookup"><span data-stu-id="b23d1-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="b23d1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b23d1-109">EXAMPLES</span></span>

### <span data-ttu-id="b23d1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b23d1-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="b23d1-111">Ustawia kontekst magazynu dla określonego magazynu usług odzyskiwania dla kolejnych operacji odzyskiwania witryny platformy Azure w bieżącej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b23d1-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="b23d1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b23d1-112">PARAMETERS</span></span>

### <span data-ttu-id="b23d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23d1-113">-DefaultProfile</span></span>
<span data-ttu-id="b23d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b23d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b23d1-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b23d1-115">-ResourceId</span></span>
<span data-ttu-id="b23d1-116">Określa identyfikator zasobu magazynu recoveryservices, który ma zostać ustawiony jako kontekst magazynu.</span><span class="sxs-lookup"><span data-stu-id="b23d1-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b23d1-117">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="b23d1-117">-Vault</span></span>
<span data-ttu-id="b23d1-118">Obiekt magazynu usług Recovery Services odpowiadający magazynowi usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b23d1-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b23d1-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b23d1-119">-Confirm</span></span>
<span data-ttu-id="b23d1-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b23d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b23d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b23d1-121">-WhatIf</span></span>
<span data-ttu-id="b23d1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b23d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b23d1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b23d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b23d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23d1-124">CommonParameters</span></span>
<span data-ttu-id="b23d1-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b23d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23d1-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b23d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23d1-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b23d1-127">INPUTS</span></span>

### <span data-ttu-id="b23d1-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="b23d1-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b23d1-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b23d1-129">OUTPUTS</span></span>

### <span data-ttu-id="b23d1-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b23d1-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b23d1-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b23d1-131">NOTES</span></span>

## <span data-ttu-id="b23d1-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b23d1-132">RELATED LINKS</span></span>
