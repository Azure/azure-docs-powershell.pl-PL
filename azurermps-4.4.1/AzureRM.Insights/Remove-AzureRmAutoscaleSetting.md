---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550992"
---
# <span data-ttu-id="4ea16-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4ea16-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="4ea16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ea16-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea16-103">Usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="4ea16-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ea16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ea16-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ea16-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea16-106">Polecenie cmdlet **Remove-AzureRmAutoscaleSetting** usuwa ustawienie skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="4ea16-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="4ea16-107">Musisz określić nazwę ustawienia oraz nazwę grupy zasobów, do której jest przypisana.</span><span class="sxs-lookup"><span data-stu-id="4ea16-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="4ea16-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ea16-108">EXAMPLES</span></span>

## <span data-ttu-id="4ea16-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ea16-109">PARAMETERS</span></span>

### <span data-ttu-id="4ea16-110">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ea16-110">-Name</span></span>
<span data-ttu-id="4ea16-111">Określa nazwę ustawienia skalowania automatycznego, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="4ea16-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea16-112">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4ea16-112">-ResourceGroup</span></span>
<span data-ttu-id="4ea16-113">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ea16-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ea16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea16-114">-DefaultProfile</span></span>
<span data-ttu-id="4ea16-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea16-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea16-116">CommonParameters</span></span>
<span data-ttu-id="4ea16-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea16-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea16-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ea16-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea16-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ea16-119">INPUTS</span></span>

## <span data-ttu-id="4ea16-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ea16-120">OUTPUTS</span></span>

### <span data-ttu-id="4ea16-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4ea16-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4ea16-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ea16-122">NOTES</span></span>

## <span data-ttu-id="4ea16-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ea16-123">RELATED LINKS</span></span>

[<span data-ttu-id="4ea16-124">Dodaj-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4ea16-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="4ea16-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="4ea16-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


