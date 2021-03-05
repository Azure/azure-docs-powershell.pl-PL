---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d19455e4b467846ce38541ca3b0ec02f586cf226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970033"
---
# <span data-ttu-id="548a7-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="548a7-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="548a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548a7-102">SYNOPSIS</span></span>
<span data-ttu-id="548a7-103">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego centrum vCenter.</span><span class="sxs-lookup"><span data-stu-id="548a7-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="548a7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="548a7-104">SYNTAX</span></span>

### <span data-ttu-id="548a7-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="548a7-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548a7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="548a7-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548a7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="548a7-107">DESCRIPTION</span></span>
<span data-ttu-id="548a7-108">Polecenie **cmdlet Update-AzRecoveryServicesAsrvCenter** aktualizuje szczegóły odnajdowania dla zarejestrowanego centrum vCenter.</span><span class="sxs-lookup"><span data-stu-id="548a7-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="548a7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="548a7-109">EXAMPLES</span></span>

### <span data-ttu-id="548a7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="548a7-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="548a7-111">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego centrum vCenter.</span><span class="sxs-lookup"><span data-stu-id="548a7-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="548a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="548a7-112">PARAMETERS</span></span>

### <span data-ttu-id="548a7-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="548a7-113">-Account</span></span>
<span data-ttu-id="548a7-114">konto poświadczeń logowania w centrum vCenter.</span><span class="sxs-lookup"><span data-stu-id="548a7-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="548a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548a7-115">-DefaultProfile</span></span>
<span data-ttu-id="548a7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="548a7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="548a7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="548a7-117">-InputObject</span></span>
<span data-ttu-id="548a7-118">Obiekt serwera vCenter do aktualizowania szczegółów odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="548a7-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="548a7-119">— Port</span><span class="sxs-lookup"><span data-stu-id="548a7-119">-Port</span></span>
<span data-ttu-id="548a7-120">Port TCP na serwerze vCenter, który ma być używany do odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="548a7-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="548a7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548a7-121">-ResourceId</span></span>
<span data-ttu-id="548a7-122">Określa wartość resourceId centrum vCenter.</span><span class="sxs-lookup"><span data-stu-id="548a7-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="548a7-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="548a7-123">-Confirm</span></span>
<span data-ttu-id="548a7-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="548a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548a7-125">-WhatIf</span></span>
<span data-ttu-id="548a7-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548a7-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="548a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548a7-128">CommonParameters</span></span>
<span data-ttu-id="548a7-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548a7-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="548a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548a7-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="548a7-131">INPUTS</span></span>

### <span data-ttu-id="548a7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="548a7-132">System.String</span></span>

### <span data-ttu-id="548a7-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="548a7-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="548a7-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="548a7-134">OUTPUTS</span></span>

### <span data-ttu-id="548a7-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="548a7-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="548a7-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="548a7-136">NOTES</span></span>

## <span data-ttu-id="548a7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="548a7-137">RELATED LINKS</span></span>
