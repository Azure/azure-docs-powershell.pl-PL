---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232509"
---
# <span data-ttu-id="aefcf-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="aefcf-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="aefcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aefcf-102">SYNOPSIS</span></span>
<span data-ttu-id="aefcf-103">Usuwa określone mapowanie kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="aefcf-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="aefcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aefcf-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefcf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aefcf-105">DESCRIPTION</span></span>
<span data-ttu-id="aefcf-106">Polecenie cmdlet **Remove-AzRecoveryServicesAsrProtectionContainerMapping** umożliwia usunięcie określonego mapowania kontenera ochrony usługi Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="aefcf-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="aefcf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aefcf-107">EXAMPLES</span></span>

### <span data-ttu-id="aefcf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aefcf-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="aefcf-109">Rozpoczyna usuwanie określonego mapowania kontenera ochrony i zwraca zadanie ASR użyte do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="aefcf-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="aefcf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aefcf-110">PARAMETERS</span></span>

### <span data-ttu-id="aefcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefcf-111">-DefaultProfile</span></span>
<span data-ttu-id="aefcf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aefcf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aefcf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="aefcf-113">-Force</span></span>
<span data-ttu-id="aefcf-114">Wymuś uruchomienie polecenia bez podania dodatkowego ostrzeżenia.</span><span class="sxs-lookup"><span data-stu-id="aefcf-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="aefcf-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aefcf-115">-InputObject</span></span>
<span data-ttu-id="aefcf-116">Obiekt wejściowy do polecenia cmdlet: obiekt mapowania kontenera ochrony ASR odpowiadający kontenerowi ochrony, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="aefcf-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="aefcf-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aefcf-117">-Confirm</span></span>
<span data-ttu-id="aefcf-118">Określ, czy potwierdzenie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="aefcf-118">Specify if confirmation is required.</span></span> <span data-ttu-id="aefcf-119">Ustaw wartość parametru Confirm na $false, aby pominąć potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aefcf-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="aefcf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefcf-120">-WhatIf</span></span>
<span data-ttu-id="aefcf-121">Pokazuje, co się stanie, jeśli jest wykonywane polecenie cmdlet bez faktycznego wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aefcf-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="aefcf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefcf-122">CommonParameters</span></span>
<span data-ttu-id="aefcf-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefcf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefcf-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aefcf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefcf-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aefcf-125">INPUTS</span></span>

### <span data-ttu-id="aefcf-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="aefcf-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="aefcf-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aefcf-127">OUTPUTS</span></span>

### <span data-ttu-id="aefcf-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="aefcf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="aefcf-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aefcf-129">NOTES</span></span>

## <span data-ttu-id="aefcf-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aefcf-130">RELATED LINKS</span></span>

[<span data-ttu-id="aefcf-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="aefcf-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="aefcf-132">Nowe — AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="aefcf-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
