---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3ab29642bcf9a6ba42f211705f3d5c2c6973a061
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708596"
---
# <span data-ttu-id="56142-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56142-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="56142-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56142-102">SYNOPSIS</span></span>
<span data-ttu-id="56142-103">Usuwa/wyrejestrowuje określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="56142-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="56142-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56142-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56142-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56142-105">DESCRIPTION</span></span>
<span data-ttu-id="56142-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrServicesProvider** usuwa określonego dostawcę usług odzyskiwania usługi Azure Site Recovery z magazynu.</span><span class="sxs-lookup"><span data-stu-id="56142-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="56142-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56142-107">EXAMPLES</span></span>

### <span data-ttu-id="56142-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56142-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="56142-109">Rozpoczyna usuwanie/Wyrejestrowanie określonego dostawcy usług Azure Site Recovery Services i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="56142-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="56142-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56142-110">PARAMETERS</span></span>

### <span data-ttu-id="56142-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56142-111">-DefaultProfile</span></span>
<span data-ttu-id="56142-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56142-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="56142-113">-Force</span><span class="sxs-lookup"><span data-stu-id="56142-113">-Force</span></span>
<span data-ttu-id="56142-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="56142-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="56142-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="56142-115">-InputObject</span></span>
<span data-ttu-id="56142-116">Obiekt wejściowy do polecenia cmdlet: obiekt dostawcy usług odzyskiwania ASR odpowiadający dostawcy usług odzyskiwania ASR, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="56142-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="56142-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56142-117">-Confirm</span></span>
<span data-ttu-id="56142-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="56142-118">Specify if confirmation is required.</span></span> <span data-ttu-id="56142-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="56142-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="56142-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56142-120">-WhatIf</span></span>
<span data-ttu-id="56142-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56142-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="56142-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56142-122">CommonParameters</span></span>
<span data-ttu-id="56142-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56142-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56142-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56142-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56142-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56142-125">INPUTS</span></span>

### <span data-ttu-id="56142-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56142-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="56142-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56142-127">OUTPUTS</span></span>

### <span data-ttu-id="56142-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="56142-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="56142-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56142-129">NOTES</span></span>

## <span data-ttu-id="56142-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56142-130">RELATED LINKS</span></span>

[<span data-ttu-id="56142-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56142-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="56142-132">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="56142-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)