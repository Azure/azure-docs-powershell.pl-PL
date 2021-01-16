---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355669"
---
# <span data-ttu-id="943c9-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="943c9-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="943c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="943c9-102">SYNOPSIS</span></span>
<span data-ttu-id="943c9-103">Usuwa określone zasady replikacji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="943c9-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="943c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="943c9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="943c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="943c9-105">DESCRIPTION</span></span>
<span data-ttu-id="943c9-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrPolicy** usunęło określone zasady replikacji z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="943c9-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="943c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="943c9-107">EXAMPLES</span></span>

### <span data-ttu-id="943c9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="943c9-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="943c9-109">Rozpoczyna usuwanie określonych zasad replikacji i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="943c9-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="943c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="943c9-110">PARAMETERS</span></span>

### <span data-ttu-id="943c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943c9-111">-DefaultProfile</span></span>
<span data-ttu-id="943c9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="943c9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="943c9-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="943c9-113">-InputObject</span></span>
<span data-ttu-id="943c9-114">Obiekt wejściowy do polecenia cmdlet: obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="943c9-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="943c9-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="943c9-115">-Confirm</span></span>
<span data-ttu-id="943c9-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943c9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943c9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943c9-117">-WhatIf</span></span>
<span data-ttu-id="943c9-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="943c9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="943c9-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="943c9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943c9-120">CommonParameters</span></span>
<span data-ttu-id="943c9-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="943c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943c9-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="943c9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943c9-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="943c9-123">INPUTS</span></span>

### <span data-ttu-id="943c9-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="943c9-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="943c9-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="943c9-125">OUTPUTS</span></span>

### <span data-ttu-id="943c9-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="943c9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="943c9-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="943c9-127">NOTES</span></span>

## <span data-ttu-id="943c9-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="943c9-128">RELATED LINKS</span></span>

[<span data-ttu-id="943c9-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="943c9-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="943c9-130">Nowe — AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="943c9-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
