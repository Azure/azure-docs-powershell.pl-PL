---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232511"
---
# <span data-ttu-id="fa3ff-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fa3ff-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="fa3ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="fa3ff-103">Usuwa określony kontener ochrony z tkaniny.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="fa3ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa3ff-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa3ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa3ff-105">DESCRIPTION</span></span>
<span data-ttu-id="fa3ff-106">Polecenie cmdlet Remove-AzRecoveryServicesAsrProtectionContainer powoduje usunięcie określonego kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="fa3ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa3ff-107">EXAMPLES</span></span>

### <span data-ttu-id="fa3ff-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fa3ff-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="fa3ff-109">Rozpoczyna usuwanie określonego kontenera ochrony i zwraca zadanie ASR użyte do śledzenia operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="fa3ff-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa3ff-110">PARAMETERS</span></span>

### <span data-ttu-id="fa3ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa3ff-111">-DefaultProfile</span></span>
<span data-ttu-id="fa3ff-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa3ff-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa3ff-113">-InputObject</span></span>
<span data-ttu-id="fa3ff-114">Określa kontener ochrony, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa3ff-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa3ff-115">-Confirm</span></span>
<span data-ttu-id="fa3ff-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa3ff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa3ff-117">-WhatIf</span></span>
<span data-ttu-id="fa3ff-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa3ff-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa3ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa3ff-120">CommonParameters</span></span>
<span data-ttu-id="fa3ff-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa3ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa3ff-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa3ff-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa3ff-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa3ff-123">INPUTS</span></span>

### <span data-ttu-id="fa3ff-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="fa3ff-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="fa3ff-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa3ff-125">OUTPUTS</span></span>

### <span data-ttu-id="fa3ff-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fa3ff-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fa3ff-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa3ff-127">NOTES</span></span>

## <span data-ttu-id="fa3ff-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa3ff-128">RELATED LINKS</span></span>
