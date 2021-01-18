---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502625"
---
# <span data-ttu-id="fc4e4-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc4e4-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="fc4e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4e4-103">Usuwa/wyrejestrowuje określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="fc4e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc4e4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc4e4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc4e4-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** usuwa określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="fc4e4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc4e4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc4e4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc4e4-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="fc4e4-109">Rozpoczyna usuwanie/Wyrejestrowanie określonego dostawcy usług Azure Site Recovery Services i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fc4e4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc4e4-110">PARAMETERS</span></span>

### <span data-ttu-id="fc4e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4e4-111">-DefaultProfile</span></span>
<span data-ttu-id="fc4e4-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fc4e4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fc4e4-113">-Force</span></span>
<span data-ttu-id="fc4e4-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="fc4e4-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc4e4-115">-InputObject</span></span>
<span data-ttu-id="fc4e4-116">Obiekt wejściowy do polecenia cmdlet: obiekt dostawcy usług odzyskiwania ASR odpowiadający dostawcy usług odzyskiwania ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4e4-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc4e4-117">-Confirm</span></span>
<span data-ttu-id="fc4e4-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-118">Specify if confirmation is required.</span></span> <span data-ttu-id="fc4e4-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="fc4e4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4e4-120">-WhatIf</span></span>
<span data-ttu-id="fc4e4-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="fc4e4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4e4-122">CommonParameters</span></span>
<span data-ttu-id="fc4e4-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4e4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4e4-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc4e4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4e4-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc4e4-125">INPUTS</span></span>

### <span data-ttu-id="fc4e4-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc4e4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="fc4e4-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc4e4-127">OUTPUTS</span></span>

### <span data-ttu-id="fc4e4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fc4e4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fc4e4-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc4e4-129">NOTES</span></span>

## <span data-ttu-id="fc4e4-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc4e4-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc4e4-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc4e4-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="fc4e4-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fc4e4-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
