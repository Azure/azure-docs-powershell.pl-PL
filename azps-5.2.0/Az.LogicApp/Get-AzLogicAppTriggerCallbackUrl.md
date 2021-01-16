---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351493"
---
# <span data-ttu-id="8d8a7-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="8d8a7-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="8d8a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8a7-103">Pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="8d8a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d8a7-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d8a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8d8a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8a7-106">Polecenie cmdlet **Get-AzLogicAppTriggerCallbackUrl** Pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="8d8a7-107">To polecenie cmdlet zwraca obiekt **WorkflowTriggerCallbackUrl** reprezentujący adres URL wywołania zwrotnego.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="8d8a7-108">Określ nazwę grupy zasobów, nazwę aplikacji logicznej i nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="8d8a7-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d8a7-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d8a7-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d8a7-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d8a7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d8a7-113">EXAMPLES</span></span>

### <span data-ttu-id="8d8a7-114">Przykład 1: Uzyskaj adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej</span><span class="sxs-lookup"><span data-stu-id="8d8a7-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="8d8a7-115">To polecenie pobiera adres URL wywołania zwrotnego wyzwalacza aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="8d8a7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d8a7-116">PARAMETERS</span></span>

### <span data-ttu-id="8d8a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8a7-117">-DefaultProfile</span></span>
<span data-ttu-id="8d8a7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8d8a7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d8a7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8d8a7-119">-Name</span></span>
<span data-ttu-id="8d8a7-120">Określa nazwę aplikacji logicznej.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="8d8a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d8a7-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d8a7-123">-Triggername</span><span class="sxs-lookup"><span data-stu-id="8d8a7-123">-TriggerName</span></span>
<span data-ttu-id="8d8a7-124">Określa nazwę wyzwalacza.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="8d8a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8a7-125">CommonParameters</span></span>
<span data-ttu-id="8d8a7-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8a7-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d8a7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8a7-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d8a7-128">INPUTS</span></span>

### <span data-ttu-id="8d8a7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8a7-129">System.String</span></span>

## <span data-ttu-id="8d8a7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d8a7-130">OUTPUTS</span></span>

### <span data-ttu-id="8d8a7-131">Microsoft. Azure. Management. Logic. MODELES. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="8d8a7-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="8d8a7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d8a7-132">NOTES</span></span>

## <span data-ttu-id="8d8a7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d8a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d8a7-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="8d8a7-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


