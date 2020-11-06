---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 856a316104e0e660f170de8f519dbcb66c55bd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552591"
---
# <span data-ttu-id="83779-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="83779-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="83779-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83779-102">SYNOPSIS</span></span>
<span data-ttu-id="83779-103">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="83779-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83779-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83779-104">SYNTAX</span></span>

### <span data-ttu-id="83779-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="83779-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83779-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83779-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83779-107">Opis</span><span class="sxs-lookup"><span data-stu-id="83779-107">DESCRIPTION</span></span>
<span data-ttu-id="83779-108">Polecenie cmdlet **Update-AzureRmRecoveryServicesAsrvCenter** jest aktualizacją szczegółów wykrywania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="83779-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="83779-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83779-109">EXAMPLES</span></span>

### <span data-ttu-id="83779-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="83779-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="83779-111">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="83779-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="83779-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83779-112">PARAMETERS</span></span>

### <span data-ttu-id="83779-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="83779-113">-Account</span></span>
<span data-ttu-id="83779-114">konto z poświadczeniami logowania vCenter.</span><span class="sxs-lookup"><span data-stu-id="83779-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83779-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83779-115">-DefaultProfile</span></span>
<span data-ttu-id="83779-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83779-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83779-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="83779-117">-InputObject</span></span>
<span data-ttu-id="83779-118">Obiekt serwera vCenter, dla którego mają zostać zaktualizowane szczegóły dotyczące odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="83779-118">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83779-119">-Port</span><span class="sxs-lookup"><span data-stu-id="83779-119">-Port</span></span>
<span data-ttu-id="83779-120">Port TCP serwera vCenter, który ma być używany do odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="83779-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83779-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83779-121">-ResourceId</span></span>
<span data-ttu-id="83779-122">Określa identyfikator zasobu vCenter.</span><span class="sxs-lookup"><span data-stu-id="83779-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="83779-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83779-123">-Confirm</span></span>
<span data-ttu-id="83779-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83779-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83779-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83779-125">-WhatIf</span></span>
<span data-ttu-id="83779-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83779-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83779-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83779-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83779-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83779-128">CommonParameters</span></span>
<span data-ttu-id="83779-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83779-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83779-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83779-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83779-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83779-131">INPUTS</span></span>

### <span data-ttu-id="83779-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="83779-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="83779-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83779-133">OUTPUTS</span></span>

### <span data-ttu-id="83779-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="83779-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83779-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83779-135">NOTES</span></span>

## <span data-ttu-id="83779-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83779-136">RELATED LINKS</span></span>
