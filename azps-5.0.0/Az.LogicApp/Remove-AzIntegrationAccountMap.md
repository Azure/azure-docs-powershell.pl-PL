---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233433"
---
# <span data-ttu-id="85937-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="85937-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="85937-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="85937-102">SYNOPSIS</span></span>
<span data-ttu-id="85937-103">Usuwa mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="85937-103">Removes an integration account map.</span></span>

## <span data-ttu-id="85937-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="85937-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85937-105">Opis</span><span class="sxs-lookup"><span data-stu-id="85937-105">DESCRIPTION</span></span>
<span data-ttu-id="85937-106">Polecenie cmdlet **Remove-AzIntegrationAccountMap** umożliwia usunięcie mapy konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85937-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="85937-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="85937-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="85937-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="85937-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="85937-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="85937-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="85937-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="85937-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="85937-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="85937-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="85937-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="85937-112">EXAMPLES</span></span>

### <span data-ttu-id="85937-113">Przykład 1: usuwanie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="85937-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="85937-114">To polecenie powoduje usunięcie mapy kont integracji o nazwie IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="85937-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="85937-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="85937-115">PARAMETERS</span></span>

### <span data-ttu-id="85937-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85937-116">-DefaultProfile</span></span>
<span data-ttu-id="85937-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="85937-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85937-118">-Force</span><span class="sxs-lookup"><span data-stu-id="85937-118">-Force</span></span>
<span data-ttu-id="85937-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="85937-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85937-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="85937-120">-MapName</span></span>
<span data-ttu-id="85937-121">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="85937-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85937-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="85937-122">-Name</span></span>
<span data-ttu-id="85937-123">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="85937-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85937-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85937-124">-ResourceGroupName</span></span>
<span data-ttu-id="85937-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85937-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85937-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85937-126">-Confirm</span></span>
<span data-ttu-id="85937-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85937-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85937-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85937-128">-WhatIf</span></span>
<span data-ttu-id="85937-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85937-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85937-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="85937-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85937-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85937-131">CommonParameters</span></span>
<span data-ttu-id="85937-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85937-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85937-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85937-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85937-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85937-134">INPUTS</span></span>

### <span data-ttu-id="85937-135">System. String</span><span class="sxs-lookup"><span data-stu-id="85937-135">System.String</span></span>

## <span data-ttu-id="85937-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="85937-136">OUTPUTS</span></span>

### <span data-ttu-id="85937-137">System. void</span><span class="sxs-lookup"><span data-stu-id="85937-137">System.Void</span></span>

## <span data-ttu-id="85937-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="85937-138">NOTES</span></span>

## <span data-ttu-id="85937-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85937-139">RELATED LINKS</span></span>

[<span data-ttu-id="85937-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="85937-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="85937-141">Nowe — AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="85937-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="85937-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="85937-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


