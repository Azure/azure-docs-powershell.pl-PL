---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183842"
---
# <span data-ttu-id="69164-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="69164-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="69164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69164-102">SYNOPSIS</span></span>
<span data-ttu-id="69164-103">Odświeża (odśwież serwer) informacje otrzymane od dostawcy usług Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="69164-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="69164-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69164-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69164-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="69164-105">DESCRIPTION</span></span>
<span data-ttu-id="69164-106">Polecenie **cmdlet Update-AzRecoveryServicesAsrServicesProvider** aktualizuje informacje otrzymane od dostawcy usług azure site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="69164-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="69164-107">To polecenie cmdlet umożliwia wyzwalanie odświeżania informacji otrzymywanych od dostawcy usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="69164-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="69164-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69164-108">EXAMPLES</span></span>

### <span data-ttu-id="69164-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69164-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="69164-110">Rozpoczyna operację odświeżania informacji od określonego dostawcy usług ASR i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="69164-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="69164-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69164-111">PARAMETERS</span></span>

### <span data-ttu-id="69164-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69164-112">-DefaultProfile</span></span>
<span data-ttu-id="69164-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69164-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="69164-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69164-114">-InputObject</span></span>
<span data-ttu-id="69164-115">Określa obiekt dostawcy usług ASR identyfikujący serwer, dla którego informacje mają zostać zaktualizowane (odświeżone).</span><span class="sxs-lookup"><span data-stu-id="69164-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="69164-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69164-116">-Confirm</span></span>
<span data-ttu-id="69164-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69164-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69164-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69164-118">-WhatIf</span></span>
<span data-ttu-id="69164-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69164-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69164-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69164-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69164-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69164-121">CommonParameters</span></span>
<span data-ttu-id="69164-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69164-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69164-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69164-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69164-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69164-124">INPUTS</span></span>

### <span data-ttu-id="69164-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="69164-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="69164-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69164-126">OUTPUTS</span></span>

### <span data-ttu-id="69164-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="69164-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="69164-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69164-128">NOTES</span></span>

## <span data-ttu-id="69164-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69164-129">RELATED LINKS</span></span>

[<span data-ttu-id="69164-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="69164-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="69164-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="69164-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
