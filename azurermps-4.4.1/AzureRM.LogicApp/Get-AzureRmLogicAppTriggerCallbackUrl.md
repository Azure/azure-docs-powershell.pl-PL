---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: f9ac8c7d7131b53b04e7da03eeb17aea33507258
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550959"
---
# <span data-ttu-id="38da4-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="38da4-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="38da4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38da4-102">SYNOPSIS</span></span>
<span data-ttu-id="38da4-103">Pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="38da4-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38da4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38da4-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38da4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38da4-105">DESCRIPTION</span></span>
<span data-ttu-id="38da4-106">Polecenie cmdlet **Get-AzureRmLogicAppTriggerCallbackUrl** Pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38da4-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="38da4-107">To polecenie cmdlet zwraca obiekt **WorkflowTriggerCallbackUrl** reprezentujący adres URL wywołania zwrotnego.</span><span class="sxs-lookup"><span data-stu-id="38da4-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="38da4-108">Określ nazwę grupy zasobów, nazwę aplikacji logicznej i nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="38da4-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="38da4-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="38da4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="38da4-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="38da4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="38da4-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="38da4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="38da4-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="38da4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="38da4-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38da4-113">EXAMPLES</span></span>

### <span data-ttu-id="38da4-114">Przykład 1: Uzyskaj adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="38da4-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="38da4-115">To polecenie pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="38da4-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="38da4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38da4-116">PARAMETERS</span></span>

### <span data-ttu-id="38da4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38da4-117">-Name</span></span>
<span data-ttu-id="38da4-118">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="38da4-118">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38da4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38da4-119">-ResourceGroupName</span></span>
<span data-ttu-id="38da4-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="38da4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="38da4-121">-Triggername</span><span class="sxs-lookup"><span data-stu-id="38da4-121">-TriggerName</span></span>
<span data-ttu-id="38da4-122">Określa nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="38da4-122">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="38da4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38da4-123">-DefaultProfile</span></span>
<span data-ttu-id="38da4-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38da4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38da4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38da4-125">CommonParameters</span></span>
<span data-ttu-id="38da4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38da4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38da4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38da4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38da4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38da4-128">INPUTS</span></span>

## <span data-ttu-id="38da4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38da4-129">OUTPUTS</span></span>

### <span data-ttu-id="38da4-130">Microsoft. Azure. Management. Logic. MODELES. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="38da4-130">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="38da4-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38da4-131">NOTES</span></span>

## <span data-ttu-id="38da4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38da4-132">RELATED LINKS</span></span>

[<span data-ttu-id="38da4-133">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="38da4-133">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)


