---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223203"
---
# <span data-ttu-id="ac707-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="ac707-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="ac707-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ac707-102">SYNOPSIS</span></span>
<span data-ttu-id="ac707-103">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="ac707-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="ac707-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ac707-104">SYNTAX</span></span>

### <span data-ttu-id="ac707-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="ac707-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac707-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac707-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac707-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ac707-107">DESCRIPTION</span></span>
<span data-ttu-id="ac707-108">Polecenie cmdlet **Update-AzRecoveryServicesAsrvCenter** jest aktualizacją szczegółów wykrywania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="ac707-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="ac707-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ac707-109">EXAMPLES</span></span>

### <span data-ttu-id="ac707-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ac707-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="ac707-111">Aktualizowanie szczegółów odnajdowania dla zarejestrowanego vCenter.</span><span class="sxs-lookup"><span data-stu-id="ac707-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="ac707-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ac707-112">PARAMETERS</span></span>

### <span data-ttu-id="ac707-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="ac707-113">-Account</span></span>
<span data-ttu-id="ac707-114">konto z poświadczeniami logowania vCenter.</span><span class="sxs-lookup"><span data-stu-id="ac707-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="ac707-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac707-115">-DefaultProfile</span></span>
<span data-ttu-id="ac707-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac707-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac707-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac707-117">-InputObject</span></span>
<span data-ttu-id="ac707-118">Obiekt serwera vCenter, dla którego mają zostać zaktualizowane szczegóły dotyczące odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="ac707-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="ac707-119">-Port</span><span class="sxs-lookup"><span data-stu-id="ac707-119">-Port</span></span>
<span data-ttu-id="ac707-120">Port TCP serwera vCenter, który ma być używany do odnajdowania.</span><span class="sxs-lookup"><span data-stu-id="ac707-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="ac707-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac707-121">-ResourceId</span></span>
<span data-ttu-id="ac707-122">Określa identyfikator zasobu vCenter.</span><span class="sxs-lookup"><span data-stu-id="ac707-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="ac707-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac707-123">-Confirm</span></span>
<span data-ttu-id="ac707-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac707-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac707-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac707-125">-WhatIf</span></span>
<span data-ttu-id="ac707-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac707-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac707-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ac707-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac707-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac707-128">CommonParameters</span></span>
<span data-ttu-id="ac707-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac707-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac707-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac707-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac707-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac707-131">INPUTS</span></span>

### <span data-ttu-id="ac707-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ac707-132">System.String</span></span>

### <span data-ttu-id="ac707-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="ac707-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="ac707-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ac707-134">OUTPUTS</span></span>

### <span data-ttu-id="ac707-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ac707-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ac707-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ac707-136">NOTES</span></span>

## <span data-ttu-id="ac707-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac707-137">RELATED LINKS</span></span>
