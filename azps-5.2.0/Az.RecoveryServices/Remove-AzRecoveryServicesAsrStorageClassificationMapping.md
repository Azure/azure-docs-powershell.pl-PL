---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8dcab2bcaeafbc5304de72b8bcf539a6f4a53934
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327171"
---
# <span data-ttu-id="24e28-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="24e28-101">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="24e28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24e28-102">SYNOPSIS</span></span>
<span data-ttu-id="24e28-103">Usuwa określone mapowanie klasyfikacji magazynu ASR.</span><span class="sxs-lookup"><span data-stu-id="24e28-103">Deletes the specified ASR storage classification mapping.</span></span>

## <span data-ttu-id="24e28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24e28-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="24e28-105">DESCRIPTION</span></span>
<span data-ttu-id="24e28-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrStorageClassificationMapping** usuwa określone mapowanie klasyfikacji magazynu odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="24e28-106">The **Remove-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="24e28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24e28-107">EXAMPLES</span></span>

### <span data-ttu-id="24e28-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="24e28-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="24e28-109">Rozpoczyna usuwanie określonego mapowania klasyfikacji magazynu i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="24e28-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="24e28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24e28-110">PARAMETERS</span></span>

### <span data-ttu-id="24e28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e28-111">-DefaultProfile</span></span>
<span data-ttu-id="24e28-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24e28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="24e28-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24e28-113">-InputObject</span></span>
<span data-ttu-id="24e28-114">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania klasyfikacji magazynu ASR odpowiadający mapowaniu klasyfikacji magazynu ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="24e28-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

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

### <span data-ttu-id="24e28-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24e28-115">-Confirm</span></span>
<span data-ttu-id="24e28-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e28-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e28-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e28-117">-WhatIf</span></span>
<span data-ttu-id="24e28-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e28-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24e28-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24e28-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e28-120">CommonParameters</span></span>
<span data-ttu-id="24e28-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e28-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24e28-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e28-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24e28-123">INPUTS</span></span>

### <span data-ttu-id="24e28-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="24e28-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="24e28-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24e28-125">OUTPUTS</span></span>

### <span data-ttu-id="24e28-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="24e28-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="24e28-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24e28-127">NOTES</span></span>

## <span data-ttu-id="24e28-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24e28-128">RELATED LINKS</span></span>

[<span data-ttu-id="24e28-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="24e28-129">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="24e28-130">Nowe — AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="24e28-130">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)
