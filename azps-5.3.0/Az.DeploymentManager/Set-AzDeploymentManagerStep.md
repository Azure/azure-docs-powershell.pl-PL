---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502629"
---
# <span data-ttu-id="8f034-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="8f034-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="8f034-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f034-102">SYNOPSIS</span></span>
<span data-ttu-id="8f034-103">Umożliwia zaktualizowanie kroku.</span><span class="sxs-lookup"><span data-stu-id="8f034-103">Updates the step.</span></span>

## <span data-ttu-id="8f034-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f034-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f034-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8f034-105">DESCRIPTION</span></span>
<span data-ttu-id="8f034-106">Polecenie cmdlet **Set-AzDeploymentManagerStep** aktualizuje krok z określonym obiektem kroku.</span><span class="sxs-lookup"><span data-stu-id="8f034-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="8f034-107">Polecenie cmdlet zwraca zaktualizowany obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="8f034-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="8f034-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f034-108">EXAMPLES</span></span>

### <span data-ttu-id="8f034-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f034-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="8f034-110">To polecenie umożliwia zaktualizowanie kroku, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="8f034-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="8f034-111">Krok zostanie zaktualizowany o właściwości ustawione w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="8f034-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="8f034-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f034-112">PARAMETERS</span></span>

### <span data-ttu-id="8f034-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f034-113">-DefaultProfile</span></span>
<span data-ttu-id="8f034-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f034-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f034-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8f034-115">-InputObject</span></span>
<span data-ttu-id="8f034-116">Obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="8f034-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f034-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f034-117">-Confirm</span></span>
<span data-ttu-id="8f034-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f034-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f034-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f034-119">-WhatIf</span></span>
<span data-ttu-id="8f034-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f034-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f034-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f034-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f034-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f034-122">CommonParameters</span></span>
<span data-ttu-id="8f034-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f034-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f034-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f034-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f034-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f034-125">INPUTS</span></span>

### <span data-ttu-id="8f034-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="8f034-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="8f034-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f034-127">OUTPUTS</span></span>

### <span data-ttu-id="8f034-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="8f034-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="8f034-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f034-129">NOTES</span></span>

## <span data-ttu-id="8f034-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f034-130">RELATED LINKS</span></span>
