---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 2ad9574cbd50c4100dbda7b35a64e557b195898a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051329"
---
# <span data-ttu-id="fa64a-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="fa64a-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="fa64a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa64a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa64a-103">Pobiera zasady automatycznego zamykania w laboratorium w laboratoriach DevTest.</span><span class="sxs-lookup"><span data-stu-id="fa64a-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="fa64a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa64a-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa64a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa64a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa64a-106">Polecenie cmdlet **Get-AzDtlAutoShutdownPolicy** pobiera zasady automatycznego zamykania w laboratorium, które umożliwia automatyczne wyłączanie wszystkich maszyn wirtualnych w laboratorium o określonej porze dnia.</span><span class="sxs-lookup"><span data-stu-id="fa64a-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="fa64a-107">Polecenie cmdlet zwraca wartość określającą, czy stan zasad jest włączony, oraz godzinę skonfigurowania automatycznego zamykania maszyn wirtualnych laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fa64a-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="fa64a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa64a-108">EXAMPLES</span></span>

## <span data-ttu-id="fa64a-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa64a-109">PARAMETERS</span></span>

### <span data-ttu-id="fa64a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa64a-110">-DefaultProfile</span></span>
<span data-ttu-id="fa64a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fa64a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa64a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="fa64a-112">-LabName</span></span>
<span data-ttu-id="fa64a-113">Określa nazwę laboratorium, dla którego to polecenie cmdlet pobiera zasady automatycznego zamykania.</span><span class="sxs-lookup"><span data-stu-id="fa64a-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="fa64a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa64a-114">-ResourceGroupName</span></span>
<span data-ttu-id="fa64a-115">Określa nazwę grupy zasobów, do której należy laboratorium.</span><span class="sxs-lookup"><span data-stu-id="fa64a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="fa64a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa64a-116">CommonParameters</span></span>
<span data-ttu-id="fa64a-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa64a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa64a-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa64a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa64a-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa64a-119">INPUTS</span></span>

### <span data-ttu-id="fa64a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="fa64a-120">System.String</span></span>

## <span data-ttu-id="fa64a-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa64a-121">OUTPUTS</span></span>

### <span data-ttu-id="fa64a-122">Microsoft. Azure. Commands. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="fa64a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="fa64a-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa64a-123">NOTES</span></span>

## <span data-ttu-id="fa64a-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa64a-124">RELATED LINKS</span></span>

[<span data-ttu-id="fa64a-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="fa64a-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


