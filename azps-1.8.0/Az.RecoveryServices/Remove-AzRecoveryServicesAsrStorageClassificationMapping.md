---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c76c2ebf40f360820ec3eef719b33142daacdbac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708594"
---
# <span data-ttu-id="b3084-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3084-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="b3084-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3084-102">SYNOPSIS</span></span>
<span data-ttu-id="b3084-103">Usuwa określone mapowanie klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="b3084-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="b3084-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3084-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3084-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3084-105">DESCRIPTION</span></span>
<span data-ttu-id="b3084-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** usuwa określone mapowanie klasyfikacji magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b3084-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="b3084-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3084-107">EXAMPLES</span></span>

### <span data-ttu-id="b3084-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3084-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="b3084-109">Rozpoczyna usuwanie określonego mapowania klasyfikacji magazynu i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b3084-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b3084-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3084-110">PARAMETERS</span></span>

### <span data-ttu-id="b3084-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3084-111">-DefaultProfile</span></span>
<span data-ttu-id="b3084-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3084-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b3084-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3084-113">-InputObject</span></span>
<span data-ttu-id="b3084-114">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania klasyfikacji magazynu ASR odpowiadający mapowaniu klasyfikacji magazynu ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="b3084-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3084-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3084-115">-Confirm</span></span>
<span data-ttu-id="b3084-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3084-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3084-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3084-117">-WhatIf</span></span>
<span data-ttu-id="b3084-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3084-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3084-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3084-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3084-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3084-120">CommonParameters</span></span>
<span data-ttu-id="b3084-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3084-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3084-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3084-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3084-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3084-123">INPUTS</span></span>

### <span data-ttu-id="b3084-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3084-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="b3084-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3084-125">OUTPUTS</span></span>

### <span data-ttu-id="b3084-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b3084-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b3084-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3084-127">NOTES</span></span>

## <span data-ttu-id="b3084-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3084-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3084-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3084-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="b3084-130">Nowe — AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="b3084-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)