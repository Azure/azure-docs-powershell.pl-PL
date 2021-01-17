---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345793"
---
# <span data-ttu-id="d9666-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d9666-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="d9666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9666-102">SYNOPSIS</span></span>
<span data-ttu-id="d9666-103">Odświeża (serwer odświeżania) informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9666-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="d9666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9666-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9666-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9666-105">DESCRIPTION</span></span>
<span data-ttu-id="d9666-106">Polecenie cmdlet **Update-AzRecoveryServicesAsrServicesProvider** aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d9666-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="d9666-107">Za pomocą tego polecenia cmdlet można wyzwolić odświeżenie informacji otrzymanych od dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="d9666-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="d9666-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9666-108">EXAMPLES</span></span>

### <span data-ttu-id="d9666-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9666-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="d9666-110">Rozpoczyna operację odświeżania informacji od określonego dostawcy usług ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="d9666-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d9666-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9666-111">PARAMETERS</span></span>

### <span data-ttu-id="d9666-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9666-112">-DefaultProfile</span></span>
<span data-ttu-id="d9666-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9666-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d9666-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9666-114">-InputObject</span></span>
<span data-ttu-id="d9666-115">Określa obiekt dostawcy usług ASR, który identyfikuje serwer, dla którego informacje są aktualizowane (odświeżane).</span><span class="sxs-lookup"><span data-stu-id="d9666-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="d9666-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9666-116">-Confirm</span></span>
<span data-ttu-id="d9666-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9666-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9666-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9666-118">-WhatIf</span></span>
<span data-ttu-id="d9666-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9666-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9666-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9666-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9666-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9666-121">CommonParameters</span></span>
<span data-ttu-id="d9666-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9666-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9666-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9666-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9666-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9666-124">INPUTS</span></span>

### <span data-ttu-id="d9666-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d9666-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="d9666-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9666-126">OUTPUTS</span></span>

### <span data-ttu-id="d9666-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9666-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9666-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9666-128">NOTES</span></span>

## <span data-ttu-id="d9666-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9666-129">RELATED LINKS</span></span>

[<span data-ttu-id="d9666-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d9666-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="d9666-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="d9666-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
