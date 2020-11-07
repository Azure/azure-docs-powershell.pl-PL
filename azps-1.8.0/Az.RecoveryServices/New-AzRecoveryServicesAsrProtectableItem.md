---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 57f9009ead66eb87685aaf0142c6dbd8b125f307
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708627"
---
# <span data-ttu-id="9f662-101">New-AzRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9f662-101">New-AzRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="9f662-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9f662-102">SYNOPSIS</span></span>
<span data-ttu-id="9f662-103">Dodawanie (odnajdowanie) serwera fizycznego do listy elementów, które można chronić.</span><span class="sxs-lookup"><span data-stu-id="9f662-103">Add(Discover) a physical server to the list of protectable items.</span></span>

## <span data-ttu-id="9f662-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9f662-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer> -FriendlyName <String>
 -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f662-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9f662-105">DESCRIPTION</span></span>
<span data-ttu-id="9f662-106">**Nowy-AzRecoveryServicesAsrProtectableItem** dodaje nowy element do ochrony z listy odkrytych elementów, które można chronić w kontenerze Ochrona w ramach sieci szkieletowej ASR (dotyczy tylko typu programu VMware Fabric).</span><span class="sxs-lookup"><span data-stu-id="9f662-106">The **New-AzRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="9f662-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9f662-107">EXAMPLES</span></span>

### <span data-ttu-id="9f662-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9f662-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectableItem -ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="9f662-109">Dodaj lub odkryj nową usługę odzyskiwania usługi Azure ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="9f662-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="9f662-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9f662-110">PARAMETERS</span></span>

### <span data-ttu-id="9f662-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f662-111">-DefaultProfile</span></span>
<span data-ttu-id="9f662-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9f662-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f662-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9f662-113">-FriendlyName</span></span>
<span data-ttu-id="9f662-114">Przyjazna nazwa elementu do ochrony.</span><span class="sxs-lookup"><span data-stu-id="9f662-114">Friendly name for the protectable item.</span></span>

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

### <span data-ttu-id="9f662-115">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="9f662-115">-IPAddress</span></span>
<span data-ttu-id="9f662-116">Adres IP elementu, który należy chronić.</span><span class="sxs-lookup"><span data-stu-id="9f662-116">IP address of the protectable item.</span></span>

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

### <span data-ttu-id="9f662-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="9f662-117">-OSType</span></span>
<span data-ttu-id="9f662-118">Typ systemu operacyjnego (Windows/Linux) elementu do ochrony.</span><span class="sxs-lookup"><span data-stu-id="9f662-118">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f662-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9f662-119">-ProtectionContainer</span></span>
<span data-ttu-id="9f662-120">Obiekt kontenera ochrony przed ASR, do którego ma zostać dodany element z możliwością ochrony.</span><span class="sxs-lookup"><span data-stu-id="9f662-120">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f662-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9f662-121">-Confirm</span></span>
<span data-ttu-id="9f662-122">Monituj o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f662-122">Prompt for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f662-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f662-123">-WhatIf</span></span>
<span data-ttu-id="9f662-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f662-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f662-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9f662-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f662-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f662-126">CommonParameters</span></span>
<span data-ttu-id="9f662-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f662-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f662-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f662-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f662-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9f662-129">INPUTS</span></span>

### <span data-ttu-id="9f662-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9f662-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="9f662-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9f662-131">OUTPUTS</span></span>

### <span data-ttu-id="9f662-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9f662-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9f662-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9f662-133">NOTES</span></span>

## <span data-ttu-id="9f662-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9f662-134">RELATED LINKS</span></span>