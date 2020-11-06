---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 45979620ea4067af3fc906dfd7348d27b4850f06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548044"
---
# <span data-ttu-id="99fcf-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="99fcf-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="99fcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="99fcf-103">Usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="99fcf-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99fcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99fcf-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99fcf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="99fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="99fcf-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="99fcf-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="99fcf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99fcf-107">EXAMPLES</span></span>

### <span data-ttu-id="99fcf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99fcf-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="99fcf-109">Rozpoczyna usuwanie określonej sieci szkieletowej i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="99fcf-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="99fcf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99fcf-110">PARAMETERS</span></span>

### <span data-ttu-id="99fcf-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99fcf-111">-Confirm</span></span>
<span data-ttu-id="99fcf-112">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="99fcf-112">Specify if confirmation is required.</span></span> <span data-ttu-id="99fcf-113">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99fcf-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="99fcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fcf-114">-DefaultProfile</span></span>
<span data-ttu-id="99fcf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="99fcf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="99fcf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="99fcf-116">-Force</span></span>
<span data-ttu-id="99fcf-117">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="99fcf-117">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fcf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="99fcf-118">-InputObject</span></span>
<span data-ttu-id="99fcf-119">Obiekt wejściowy do polecenia cmdlet: obiekt sieci szkieletowej ASR odpowiadający sieci szkieletowej, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="99fcf-119">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99fcf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99fcf-120">-WhatIf</span></span>
<span data-ttu-id="99fcf-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99fcf-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="99fcf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fcf-122">CommonParameters</span></span>
<span data-ttu-id="99fcf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99fcf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fcf-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fcf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fcf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99fcf-125">INPUTS</span></span>

### <span data-ttu-id="99fcf-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="99fcf-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="99fcf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99fcf-127">OUTPUTS</span></span>

### <span data-ttu-id="99fcf-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="99fcf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="99fcf-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99fcf-129">NOTES</span></span>

## <span data-ttu-id="99fcf-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99fcf-130">RELATED LINKS</span></span>

[<span data-ttu-id="99fcf-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="99fcf-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="99fcf-132">Nowe — AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="99fcf-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
