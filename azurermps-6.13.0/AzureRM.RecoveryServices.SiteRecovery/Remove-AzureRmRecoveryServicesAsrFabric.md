---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8a7b36b67b0ec1721da36dfeba920b556892c5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552075"
---
# <span data-ttu-id="23198-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="23198-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="23198-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23198-102">SYNOPSIS</span></span>
<span data-ttu-id="23198-103">Usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="23198-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23198-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23198-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23198-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23198-105">DESCRIPTION</span></span>
<span data-ttu-id="23198-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrFabric** usuwa określoną sieć szkieletową odzyskiwania witryny platformy Azure z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="23198-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="23198-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23198-107">EXAMPLES</span></span>

### <span data-ttu-id="23198-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23198-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="23198-109">Rozpoczyna usuwanie określonej sieci szkieletowej i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="23198-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="23198-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23198-110">PARAMETERS</span></span>

### <span data-ttu-id="23198-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23198-111">-DefaultProfile</span></span>
<span data-ttu-id="23198-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23198-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23198-113">-Force</span><span class="sxs-lookup"><span data-stu-id="23198-113">-Force</span></span>
<span data-ttu-id="23198-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="23198-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23198-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="23198-115">-InputObject</span></span>
<span data-ttu-id="23198-116">Obiekt wejściowy do polecenia cmdlet: obiekt sieci szkieletowej ASR odpowiadający sieci szkieletowej, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="23198-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23198-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23198-117">-Confirm</span></span>
<span data-ttu-id="23198-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="23198-118">Specify if confirmation is required.</span></span> <span data-ttu-id="23198-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="23198-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="23198-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23198-120">-WhatIf</span></span>
<span data-ttu-id="23198-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23198-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="23198-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23198-122">CommonParameters</span></span>
<span data-ttu-id="23198-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23198-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23198-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23198-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23198-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23198-125">INPUTS</span></span>

### <span data-ttu-id="23198-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="23198-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="23198-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23198-127">OUTPUTS</span></span>

### <span data-ttu-id="23198-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="23198-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="23198-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23198-129">NOTES</span></span>

## <span data-ttu-id="23198-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23198-130">RELATED LINKS</span></span>

[<span data-ttu-id="23198-131">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="23198-131">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="23198-132">Nowe — AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="23198-132">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
