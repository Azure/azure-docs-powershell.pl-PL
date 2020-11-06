---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: a7104f33fd2e5b9428b062bd8ac359ccabb25520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550952"
---
# <span data-ttu-id="b6f41-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b6f41-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="b6f41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6f41-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f41-103">Usuwa mapę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b6f41-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6f41-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6f41-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f41-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccountMap** umożliwia usunięcie mapy konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6f41-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="b6f41-107">Określ nazwę konta integracji, nazwę grupy zasobów i nazwę mapy.</span><span class="sxs-lookup"><span data-stu-id="b6f41-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="b6f41-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="b6f41-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b6f41-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="b6f41-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b6f41-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="b6f41-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b6f41-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="b6f41-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b6f41-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6f41-112">EXAMPLES</span></span>

### <span data-ttu-id="b6f41-113">Przykład 1: usuwanie mapy konta integracji</span><span class="sxs-lookup"><span data-stu-id="b6f41-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="b6f41-114">To polecenie powoduje usunięcie mapy kont integracji o nazwie IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="b6f41-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="b6f41-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6f41-115">PARAMETERS</span></span>

### <span data-ttu-id="b6f41-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6f41-116">-Force</span></span>
<span data-ttu-id="b6f41-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6f41-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6f41-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="b6f41-118">-MapName</span></span>
<span data-ttu-id="b6f41-119">Określa nazwę mapy konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b6f41-119">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="b6f41-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6f41-120">-Name</span></span>
<span data-ttu-id="b6f41-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="b6f41-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b6f41-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f41-122">-ResourceGroupName</span></span>
<span data-ttu-id="b6f41-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b6f41-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b6f41-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6f41-124">-Confirm</span></span>
<span data-ttu-id="b6f41-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f41-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f41-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f41-126">-WhatIf</span></span>
<span data-ttu-id="b6f41-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f41-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f41-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6f41-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f41-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f41-129">-DefaultProfile</span></span>
<span data-ttu-id="b6f41-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f41-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6f41-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f41-131">CommonParameters</span></span>
<span data-ttu-id="b6f41-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f41-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f41-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f41-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f41-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6f41-134">INPUTS</span></span>

## <span data-ttu-id="b6f41-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6f41-135">OUTPUTS</span></span>

## <span data-ttu-id="b6f41-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6f41-136">NOTES</span></span>

## <span data-ttu-id="b6f41-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6f41-137">RELATED LINKS</span></span>

[<span data-ttu-id="b6f41-138">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b6f41-138">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b6f41-139">Nowe — AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b6f41-139">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b6f41-140">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b6f41-140">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


