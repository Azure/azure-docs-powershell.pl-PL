---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/stop-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Stop-AzureRmAksDashboard.md
ms.openlocfilehash: 719ef5fd3676fdc5d5b6b8460bcb3edafabb83f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544012"
---
# <span data-ttu-id="62d25-101">Stop-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="62d25-101">Stop-AzureRmAksDashboard</span></span>

## <span data-ttu-id="62d25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62d25-102">SYNOPSIS</span></span>
<span data-ttu-id="62d25-103">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="62d25-103">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62d25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62d25-104">SYNTAX</span></span>

```
Stop-AzureRmAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62d25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62d25-105">DESCRIPTION</span></span>
<span data-ttu-id="62d25-106">Zatrzymaj tunel SSH Kubectl utworzony w menu Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="62d25-106">Stop the Kubectl SSH tunnel created in Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="62d25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62d25-107">EXAMPLES</span></span>

### <span data-ttu-id="62d25-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62d25-108">Example 1</span></span>
```
PS C:\> Stop-AzureRmKubernetesDashboard
```

<span data-ttu-id="62d25-109">Zatrzymuje istniejące ustawienia tunelu SSH, wykonując w menu Start-AzureRmKubernetesDashboard.</span><span class="sxs-lookup"><span data-stu-id="62d25-109">Stops the existing SSH tunnel setup by executing Start-AzureRmKubernetesDashboard.</span></span>

## <span data-ttu-id="62d25-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62d25-110">PARAMETERS</span></span>

### <span data-ttu-id="62d25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d25-111">-DefaultProfile</span></span>
<span data-ttu-id="62d25-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62d25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d25-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62d25-113">-PassThru</span></span>
<span data-ttu-id="62d25-114">Zwraca wartość PRAWDA, jeśli tunel SSH jest zamknięty.</span><span class="sxs-lookup"><span data-stu-id="62d25-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="62d25-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d25-115">CommonParameters</span></span>
<span data-ttu-id="62d25-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d25-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d25-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62d25-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d25-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62d25-118">INPUTS</span></span>

### <span data-ttu-id="62d25-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="62d25-119">None</span></span>

## <span data-ttu-id="62d25-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62d25-120">OUTPUTS</span></span>

### <span data-ttu-id="62d25-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62d25-121">System.Boolean</span></span>

## <span data-ttu-id="62d25-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62d25-122">NOTES</span></span>

## <span data-ttu-id="62d25-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62d25-123">RELATED LINKS</span></span>
