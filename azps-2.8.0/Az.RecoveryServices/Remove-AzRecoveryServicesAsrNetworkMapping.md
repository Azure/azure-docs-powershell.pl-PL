---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e4e6579c330f8ac4189db2ddfc5d3a0578fd07f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886658"
---
# <span data-ttu-id="daee4-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="daee4-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="daee4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="daee4-102">SYNOPSIS</span></span>
<span data-ttu-id="daee4-103">Usuwa określone mapowanie sieci funkcji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="daee4-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="daee4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="daee4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daee4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="daee4-105">DESCRIPTION</span></span>
<span data-ttu-id="daee4-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrNetworkMapping** umożliwia usunięcie określonego mapowania sieci funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="daee4-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="daee4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="daee4-107">EXAMPLES</span></span>

### <span data-ttu-id="daee4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="daee4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="daee4-109">Rozpoczyna usuwanie określonego mapowania sieci funkcji ASR i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="daee4-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="daee4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="daee4-110">PARAMETERS</span></span>

### <span data-ttu-id="daee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daee4-111">-DefaultProfile</span></span>
<span data-ttu-id="daee4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="daee4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="daee4-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="daee4-113">-InputObject</span></span>
<span data-ttu-id="daee4-114">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania sieci ASR odpowiadający mapowaniu sieci funkcji ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="daee4-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daee4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="daee4-115">-Confirm</span></span>
<span data-ttu-id="daee4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daee4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daee4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daee4-117">-WhatIf</span></span>
<span data-ttu-id="daee4-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daee4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="daee4-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="daee4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daee4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daee4-120">CommonParameters</span></span>
<span data-ttu-id="daee4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daee4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daee4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daee4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daee4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="daee4-123">INPUTS</span></span>

### <span data-ttu-id="daee4-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="daee4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="daee4-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="daee4-125">OUTPUTS</span></span>

### <span data-ttu-id="daee4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="daee4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="daee4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="daee4-127">NOTES</span></span>

## <span data-ttu-id="daee4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="daee4-128">RELATED LINKS</span></span>

[<span data-ttu-id="daee4-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="daee4-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="daee4-130">Nowe — AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="daee4-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
