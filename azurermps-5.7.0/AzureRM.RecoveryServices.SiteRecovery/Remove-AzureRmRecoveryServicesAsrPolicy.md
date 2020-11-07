---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: c8ef77367c66cc479bcbab25aba427c50a38447e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717318"
---
# <span data-ttu-id="ebee7-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ebee7-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ebee7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebee7-102">SYNOPSIS</span></span>
<span data-ttu-id="ebee7-103">Usuwa określone zasady replikacji ASR z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ebee7-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebee7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebee7-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebee7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebee7-105">DESCRIPTION</span></span>
<span data-ttu-id="ebee7-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrPolicy** usunęło określone zasady replikacji z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="ebee7-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="ebee7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebee7-107">EXAMPLES</span></span>

### <span data-ttu-id="ebee7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ebee7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="ebee7-109">Rozpoczyna usuwanie określonych zasad replikacji i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="ebee7-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ebee7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebee7-110">PARAMETERS</span></span>

### <span data-ttu-id="ebee7-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ebee7-111">-Confirm</span></span>
<span data-ttu-id="ebee7-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebee7-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebee7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebee7-113">-DefaultProfile</span></span>
<span data-ttu-id="ebee7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebee7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="ebee7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ebee7-115">-InputObject</span></span>
<span data-ttu-id="ebee7-116">Obiekt wejściowy do polecenia cmdlet: obiekt zasad replikacji ASR odpowiadający zasadom replikacji, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="ebee7-116">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebee7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebee7-117">-WhatIf</span></span>
<span data-ttu-id="ebee7-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebee7-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebee7-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ebee7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebee7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebee7-120">CommonParameters</span></span>
<span data-ttu-id="ebee7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebee7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebee7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebee7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebee7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebee7-123">INPUTS</span></span>

### <span data-ttu-id="ebee7-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ebee7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ebee7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebee7-125">OUTPUTS</span></span>

### <span data-ttu-id="ebee7-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="ebee7-126">System.Object</span></span>

## <span data-ttu-id="ebee7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebee7-127">NOTES</span></span>

## <span data-ttu-id="ebee7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebee7-128">RELATED LINKS</span></span>

[<span data-ttu-id="ebee7-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ebee7-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="ebee7-130">Nowe — AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ebee7-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
