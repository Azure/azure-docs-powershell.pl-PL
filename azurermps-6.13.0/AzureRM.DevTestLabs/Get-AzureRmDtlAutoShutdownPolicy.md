---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 04b226a623a31c73ddd92c858f9ab610a533886f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543879"
---
# <span data-ttu-id="c69ed-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c69ed-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="c69ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c69ed-102">SYNOPSIS</span></span>
<span data-ttu-id="c69ed-103">Pobiera zasady automatycznego zamykania w laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="c69ed-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c69ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c69ed-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69ed-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c69ed-105">DESCRIPTION</span></span>
<span data-ttu-id="c69ed-106">Polecenie cmdlet **Get-AzureRmDtlAutoShutdownPolicy** pobiera zasady automatycznego zamykania w laboratorium, które umożliwia automatyczne wyłączanie wszystkich maszyn wirtualnych w laboratorium o określonej porze dnia.</span><span class="sxs-lookup"><span data-stu-id="c69ed-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="c69ed-107">Polecenie cmdlet zwraca wartość określającą, czy stan zasad jest włączony, oraz godzinę skonfigurowania automatycznego zamykania maszyn wirtualnych laboratorium.</span><span class="sxs-lookup"><span data-stu-id="c69ed-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="c69ed-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c69ed-108">EXAMPLES</span></span>

## <span data-ttu-id="c69ed-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c69ed-109">PARAMETERS</span></span>

### <span data-ttu-id="c69ed-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69ed-110">-DefaultProfile</span></span>
<span data-ttu-id="c69ed-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c69ed-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c69ed-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="c69ed-112">-LabName</span></span>
<span data-ttu-id="c69ed-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady automatycznego zamykania.</span><span class="sxs-lookup"><span data-stu-id="c69ed-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ed-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69ed-114">-ResourceGroupName</span></span>
<span data-ttu-id="c69ed-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="c69ed-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c69ed-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69ed-116">CommonParameters</span></span>
<span data-ttu-id="c69ed-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c69ed-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69ed-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69ed-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69ed-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c69ed-119">INPUTS</span></span>

### <span data-ttu-id="c69ed-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c69ed-120">System.String</span></span>

## <span data-ttu-id="c69ed-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c69ed-121">OUTPUTS</span></span>

### <span data-ttu-id="c69ed-122">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="c69ed-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="c69ed-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c69ed-123">NOTES</span></span>

## <span data-ttu-id="c69ed-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c69ed-124">RELATED LINKS</span></span>

[<span data-ttu-id="c69ed-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="c69ed-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


