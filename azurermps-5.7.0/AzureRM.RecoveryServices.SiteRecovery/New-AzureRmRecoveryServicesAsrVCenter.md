---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 1d298a543071c879e2279734247febba00b8da21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525013"
---
# <span data-ttu-id="6a958-101">New-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="6a958-101">New-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="6a958-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a958-102">SYNOPSIS</span></span>
<span data-ttu-id="6a958-103">Dodaje serwer vCenter do odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="6a958-103">Adds a vCenter server to discover protectable items from.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a958-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a958-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount>
 -Port <Int32> -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a958-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a958-105">DESCRIPTION</span></span>
<span data-ttu-id="6a958-106">Polecenie cmdlet **New-AzureRmRecoveryServicesAsrvCenter** umożliwia dodanie serwera vCenter w celu odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="6a958-106">The **New-AzureRmRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="6a958-107">To polecenie cmdlet rejestruje serwer vCenter do odnajdowania za pomocą serwera konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="6a958-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="6a958-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a958-108">EXAMPLES</span></span>

### <span data-ttu-id="6a958-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6a958-109">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="6a958-110">Dodaje serwer vCenter do odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="6a958-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="6a958-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a958-111">PARAMETERS</span></span>

### <span data-ttu-id="6a958-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="6a958-112">-Account</span></span>
<span data-ttu-id="6a958-113">Konto creadential logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6a958-113">User login creadential Account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a958-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a958-114">-Confirm</span></span>
<span data-ttu-id="6a958-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a958-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a958-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a958-116">-DefaultProfile</span></span>
<span data-ttu-id="6a958-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a958-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a958-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6a958-118">-Fabric</span></span>
<span data-ttu-id="6a958-119">Sieć szkieletowa ASR odpowiadająca serwerowi konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="6a958-119">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a958-120">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="6a958-120">-IpOrHostName</span></span>
<span data-ttu-id="6a958-121">Adres IPv4 lub nazwa FQDN serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="6a958-121">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a958-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a958-122">-Name</span></span>
<span data-ttu-id="6a958-123">Przyjazna nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="6a958-123">A friendly name for the vCenter server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a958-124">-Port</span><span class="sxs-lookup"><span data-stu-id="6a958-124">-Port</span></span>
<span data-ttu-id="6a958-125">Port TCP serwera vCenter, który ma być używany do odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="6a958-125">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a958-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a958-126">-WhatIf</span></span>
<span data-ttu-id="6a958-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a958-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a958-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a958-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a958-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a958-129">CommonParameters</span></span>
<span data-ttu-id="6a958-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a958-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a958-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a958-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a958-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a958-132">INPUTS</span></span>

### <span data-ttu-id="6a958-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6a958-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6a958-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a958-134">OUTPUTS</span></span>

### <span data-ttu-id="6a958-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6a958-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6a958-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a958-136">NOTES</span></span>

## <span data-ttu-id="6a958-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a958-137">RELATED LINKS</span></span>
