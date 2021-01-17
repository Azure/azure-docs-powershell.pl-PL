---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 275a48f90e393f55fbd2d9df98471ce214b19a3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335773"
---
# <span data-ttu-id="2da3e-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="2da3e-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="2da3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2da3e-102">SYNOPSIS</span></span>
<span data-ttu-id="2da3e-103">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="2da3e-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="2da3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2da3e-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2da3e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2da3e-105">DESCRIPTION</span></span>
<span data-ttu-id="2da3e-106">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="2da3e-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="2da3e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2da3e-107">EXAMPLES</span></span>

### <span data-ttu-id="2da3e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2da3e-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="2da3e-109">Zatrzymuje istniejące ustawienia tunelu SSH, wykonując w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="2da3e-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="2da3e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2da3e-110">PARAMETERS</span></span>

### <span data-ttu-id="2da3e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2da3e-111">-DefaultProfile</span></span>
<span data-ttu-id="2da3e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2da3e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2da3e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2da3e-113">-PassThru</span></span>
<span data-ttu-id="2da3e-114">Zwraca wartość PRAWDA, jeśli tunel SSH jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="2da3e-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="2da3e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2da3e-115">CommonParameters</span></span>
<span data-ttu-id="2da3e-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2da3e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2da3e-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2da3e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2da3e-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2da3e-118">INPUTS</span></span>

### <span data-ttu-id="2da3e-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2da3e-119">None</span></span>

## <span data-ttu-id="2da3e-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2da3e-120">OUTPUTS</span></span>

### <span data-ttu-id="2da3e-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2da3e-121">System.Boolean</span></span>

## <span data-ttu-id="2da3e-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2da3e-122">NOTES</span></span>

## <span data-ttu-id="2da3e-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2da3e-123">RELATED LINKS</span></span>
