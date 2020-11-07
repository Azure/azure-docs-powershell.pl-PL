---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707161"
---
# <span data-ttu-id="d2cf8-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="d2cf8-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="d2cf8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cf8-103">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d2cf8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2cf8-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2cf8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="d2cf8-106">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d2cf8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2cf8-107">EXAMPLES</span></span>

### <span data-ttu-id="d2cf8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d2cf8-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="d2cf8-109">Zatrzymuje istniejące ustawienia tunelu SSH, wykonując w menu Start-AzKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="d2cf8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2cf8-110">PARAMETERS</span></span>

### <span data-ttu-id="d2cf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cf8-111">-DefaultProfile</span></span>
<span data-ttu-id="d2cf8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2cf8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2cf8-113">-PassThru</span></span>
<span data-ttu-id="d2cf8-114">Zwraca wartość PRAWDA, jeśli tunel SSH jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="d2cf8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cf8-115">CommonParameters</span></span>
<span data-ttu-id="d2cf8-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2cf8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cf8-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2cf8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cf8-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2cf8-118">INPUTS</span></span>

### <span data-ttu-id="d2cf8-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d2cf8-119">None</span></span>

## <span data-ttu-id="d2cf8-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2cf8-120">OUTPUTS</span></span>

### <span data-ttu-id="d2cf8-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2cf8-121">System.Boolean</span></span>

## <span data-ttu-id="d2cf8-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2cf8-122">NOTES</span></span>

## <span data-ttu-id="d2cf8-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2cf8-123">RELATED LINKS</span></span>
