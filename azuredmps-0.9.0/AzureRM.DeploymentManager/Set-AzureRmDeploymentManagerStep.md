---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523509"
---
# <span data-ttu-id="56985-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="56985-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="56985-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56985-102">SYNOPSIS</span></span>
<span data-ttu-id="56985-103">Umożliwia zaktualizowanie kroku.</span><span class="sxs-lookup"><span data-stu-id="56985-103">Updates a step.</span></span>

## <span data-ttu-id="56985-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56985-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56985-105">Opis</span><span class="sxs-lookup"><span data-stu-id="56985-105">DESCRIPTION</span></span>
<span data-ttu-id="56985-106">Polecenie cmdlet **Set-AzureRmDeploymentManagerStep** aktualizuje krok z określonym obiektem kroku.</span><span class="sxs-lookup"><span data-stu-id="56985-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="56985-107">Polecenie cmdlet zwraca zaktualizowany obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="56985-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="56985-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56985-108">EXAMPLES</span></span>

### <span data-ttu-id="56985-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56985-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="56985-110">To polecenie umożliwia zaktualizowanie kroku, którego nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="56985-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="56985-111">Krok zostanie zaktualizowany o właściwości ustawione w $stepObject.</span><span class="sxs-lookup"><span data-stu-id="56985-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="56985-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56985-112">PARAMETERS</span></span>

### <span data-ttu-id="56985-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56985-113">-DefaultProfile</span></span>
<span data-ttu-id="56985-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56985-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56985-115">-Krok</span><span class="sxs-lookup"><span data-stu-id="56985-115">-Step</span></span>
<span data-ttu-id="56985-116">Obiekt kroku.</span><span class="sxs-lookup"><span data-stu-id="56985-116">The step object.</span></span>

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

### <span data-ttu-id="56985-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56985-117">-Confirm</span></span>
<span data-ttu-id="56985-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56985-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56985-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56985-119">-WhatIf</span></span>
<span data-ttu-id="56985-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56985-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56985-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56985-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56985-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56985-122">CommonParameters</span></span>
<span data-ttu-id="56985-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56985-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="56985-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56985-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56985-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56985-125">INPUTS</span></span>

### <span data-ttu-id="56985-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="56985-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="56985-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56985-127">OUTPUTS</span></span>

### <span data-ttu-id="56985-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="56985-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="56985-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56985-129">NOTES</span></span>

## <span data-ttu-id="56985-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56985-130">RELATED LINKS</span></span>
