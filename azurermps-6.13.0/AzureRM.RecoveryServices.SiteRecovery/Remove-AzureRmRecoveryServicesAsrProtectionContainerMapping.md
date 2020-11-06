---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f034f91f026538bbae475466fbd9d3afa7067145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552596"
---
# <span data-ttu-id="562f6-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="562f6-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="562f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="562f6-102">SYNOPSIS</span></span>
<span data-ttu-id="562f6-103">Usuwa określone mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="562f6-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="562f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="562f6-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="562f6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="562f6-105">DESCRIPTION</span></span>
<span data-ttu-id="562f6-106">Polecenie cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** umożliwia usunięcie określonego mapowania kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="562f6-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="562f6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="562f6-107">EXAMPLES</span></span>

### <span data-ttu-id="562f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="562f6-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="562f6-109">Rozpoczyna usuwanie określonego mapowania kontenera ochrony i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="562f6-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="562f6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="562f6-110">PARAMETERS</span></span>

### <span data-ttu-id="562f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="562f6-111">-DefaultProfile</span></span>
<span data-ttu-id="562f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="562f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="562f6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="562f6-113">-Force</span></span>
<span data-ttu-id="562f6-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="562f6-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="562f6-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="562f6-115">-InputObject</span></span>
<span data-ttu-id="562f6-116">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania kontenera ochrony ASR odpowiadający kontenerowi ochrony, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="562f6-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="562f6-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="562f6-117">-Confirm</span></span>
<span data-ttu-id="562f6-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="562f6-118">Specify if confirmation is required.</span></span> <span data-ttu-id="562f6-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="562f6-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="562f6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="562f6-120">-WhatIf</span></span>
<span data-ttu-id="562f6-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="562f6-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="562f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="562f6-122">CommonParameters</span></span>
<span data-ttu-id="562f6-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="562f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="562f6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="562f6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="562f6-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="562f6-125">INPUTS</span></span>

### <span data-ttu-id="562f6-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="562f6-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="562f6-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="562f6-127">OUTPUTS</span></span>

### <span data-ttu-id="562f6-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="562f6-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="562f6-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="562f6-129">NOTES</span></span>

## <span data-ttu-id="562f6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="562f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="562f6-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="562f6-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="562f6-132">Nowe — AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="562f6-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
