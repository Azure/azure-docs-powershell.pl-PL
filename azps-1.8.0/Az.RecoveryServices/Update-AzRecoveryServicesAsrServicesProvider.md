---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 60bcdad644f07f627373c90791c8cd115d590bcd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708532"
---
# <span data-ttu-id="da7d9-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da7d9-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="da7d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="da7d9-103">Odświeża (serwer odświeżania) informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="da7d9-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="da7d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da7d9-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da7d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da7d9-105">DESCRIPTION</span></span>
<span data-ttu-id="da7d9-106">Polecenie cmdlet **Update-AzRecoveryServicesAsrServicesProvider** aktualizuje informacje otrzymane od dostawcy usług Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="da7d9-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="da7d9-107">Za pomocą tego polecenia cmdlet można wyzwolić odświeżenie informacji otrzymanych od dostawcy usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="da7d9-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="da7d9-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da7d9-108">EXAMPLES</span></span>

### <span data-ttu-id="da7d9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="da7d9-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="da7d9-110">Rozpoczyna operację odświeżania informacji od określonego dostawcy usług ASR i zwraca zadanie ASR używane do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="da7d9-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="da7d9-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da7d9-111">PARAMETERS</span></span>

### <span data-ttu-id="da7d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7d9-112">-DefaultProfile</span></span>
<span data-ttu-id="da7d9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da7d9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="da7d9-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="da7d9-114">-InputObject</span></span>
<span data-ttu-id="da7d9-115">Określa obiekt dostawcy usług ASR, który identyfikuje serwer, dla którego informacje są aktualizowane (odświeżane).</span><span class="sxs-lookup"><span data-stu-id="da7d9-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="da7d9-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da7d9-116">-Confirm</span></span>
<span data-ttu-id="da7d9-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7d9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7d9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7d9-118">-WhatIf</span></span>
<span data-ttu-id="da7d9-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7d9-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da7d9-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da7d9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7d9-121">CommonParameters</span></span>
<span data-ttu-id="da7d9-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7d9-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7d9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7d9-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da7d9-124">INPUTS</span></span>

### <span data-ttu-id="da7d9-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da7d9-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="da7d9-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da7d9-126">OUTPUTS</span></span>

### <span data-ttu-id="da7d9-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="da7d9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="da7d9-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da7d9-128">NOTES</span></span>

## <span data-ttu-id="da7d9-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da7d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="da7d9-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da7d9-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="da7d9-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="da7d9-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)