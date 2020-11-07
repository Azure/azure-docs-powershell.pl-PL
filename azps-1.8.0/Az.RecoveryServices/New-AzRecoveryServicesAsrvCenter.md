---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 98bc2dfde30357e7f6a3db62ec550a2a0c173bb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708624"
---
# <span data-ttu-id="bd53f-101">New-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="bd53f-101">New-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="bd53f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd53f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd53f-103">Dodaje serwer vCenter do odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="bd53f-103">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="bd53f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd53f-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> -Account <ASRRunAsAccount> -Port <Int32>
 -IpOrHostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd53f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd53f-105">DESCRIPTION</span></span>
<span data-ttu-id="bd53f-106">Polecenie cmdlet **New-AzRecoveryServicesAsrvCenter** umożliwia dodanie serwera vCenter w celu odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="bd53f-106">The **New-AzRecoveryServicesAsrvCenter** cmdlet adds a vCenter server to discover protectable items from.</span></span> <span data-ttu-id="bd53f-107">To polecenie cmdlet rejestruje serwer vCenter do odnajdowania za pomocą serwera konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="bd53f-107">This cmdlet registers the vCenter server for discovery with the Configuration server.</span></span>

## <span data-ttu-id="bd53f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd53f-108">EXAMPLES</span></span>

### <span data-ttu-id="bd53f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd53f-109">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrvCenterServer -Account $ConfigServer.FabricSpecificDetails.RunAsAccounts[1] -Fabric $ConfigServer -Name InmTest59 -Port 443 -Server 10.150.209.6

Asr Job for vCenter creation.
```

<span data-ttu-id="bd53f-110">Dodaje serwer vCenter do odnajdowania elementów podlegających ochronie.</span><span class="sxs-lookup"><span data-stu-id="bd53f-110">Adds a vCenter server to discover protectable items from.</span></span>

## <span data-ttu-id="bd53f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd53f-111">PARAMETERS</span></span>

### <span data-ttu-id="bd53f-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="bd53f-112">-Account</span></span>
<span data-ttu-id="bd53f-113">Konto creadential logowania użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bd53f-113">User login creadential Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd53f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd53f-114">-DefaultProfile</span></span>
<span data-ttu-id="bd53f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd53f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd53f-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="bd53f-116">-Fabric</span></span>
<span data-ttu-id="bd53f-117">Sieć szkieletowa ASR odpowiadająca serwerowi konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="bd53f-117">ASR fabric corresponding to the Configuration server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd53f-118">-IpOrHostName</span><span class="sxs-lookup"><span data-stu-id="bd53f-118">-IpOrHostName</span></span>
<span data-ttu-id="bd53f-119">Adres IPv4 lub nazwa FQDN serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="bd53f-119">IPv4 address or FQDN of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd53f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd53f-120">-Name</span></span>
<span data-ttu-id="bd53f-121">Przyjazna nazwa serwera vCenter.</span><span class="sxs-lookup"><span data-stu-id="bd53f-121">A friendly name for the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd53f-122">-Port</span><span class="sxs-lookup"><span data-stu-id="bd53f-122">-Port</span></span>
<span data-ttu-id="bd53f-123">Port TCP serwera vCenter, który ma być używany do odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="bd53f-123">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd53f-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd53f-124">-Confirm</span></span>
<span data-ttu-id="bd53f-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd53f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd53f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd53f-126">-WhatIf</span></span>
<span data-ttu-id="bd53f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd53f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd53f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd53f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd53f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd53f-129">CommonParameters</span></span>
<span data-ttu-id="bd53f-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd53f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd53f-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd53f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd53f-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd53f-132">INPUTS</span></span>

### <span data-ttu-id="bd53f-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="bd53f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="bd53f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd53f-134">OUTPUTS</span></span>

### <span data-ttu-id="bd53f-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bd53f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd53f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd53f-136">NOTES</span></span>

## <span data-ttu-id="bd53f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd53f-137">RELATED LINKS</span></span>
