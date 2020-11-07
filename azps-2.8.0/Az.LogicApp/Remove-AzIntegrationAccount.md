---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: b1833f2a87f21df7f7826ad395564fd4fe4151be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705003"
---
# <span data-ttu-id="87a6a-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="87a6a-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="87a6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="87a6a-103">Usuwa konto integracji.</span><span class="sxs-lookup"><span data-stu-id="87a6a-103">Removes an integration account.</span></span>

## <span data-ttu-id="87a6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87a6a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a6a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="87a6a-105">DESCRIPTION</span></span>
<span data-ttu-id="87a6a-106">Polecenie cmdlet **Remove-AzIntegrationAccount** umożliwia usunięcie konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87a6a-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="87a6a-107">Określ nazwę konta integracji i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87a6a-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="87a6a-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="87a6a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="87a6a-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="87a6a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="87a6a-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="87a6a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="87a6a-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="87a6a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="87a6a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87a6a-112">EXAMPLES</span></span>

### <span data-ttu-id="87a6a-113">Przykład 1: usuwanie konta integracji</span><span class="sxs-lookup"><span data-stu-id="87a6a-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="87a6a-114">To polecenie usuwa konto integracyjne o nazwie IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="87a6a-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="87a6a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87a6a-115">PARAMETERS</span></span>

### <span data-ttu-id="87a6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a6a-116">-DefaultProfile</span></span>
<span data-ttu-id="87a6a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="87a6a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87a6a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="87a6a-118">-Force</span></span>
<span data-ttu-id="87a6a-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="87a6a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87a6a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87a6a-120">-Name</span></span>
<span data-ttu-id="87a6a-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="87a6a-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="87a6a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a6a-122">-ResourceGroupName</span></span>
<span data-ttu-id="87a6a-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87a6a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="87a6a-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87a6a-124">-Confirm</span></span>
<span data-ttu-id="87a6a-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a6a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a6a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a6a-126">-WhatIf</span></span>
<span data-ttu-id="87a6a-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a6a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a6a-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="87a6a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a6a-129">CommonParameters</span></span>
<span data-ttu-id="87a6a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a6a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a6a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87a6a-132">INPUTS</span></span>

### <span data-ttu-id="87a6a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="87a6a-133">System.String</span></span>

## <span data-ttu-id="87a6a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87a6a-134">OUTPUTS</span></span>

### <span data-ttu-id="87a6a-135">System. void</span><span class="sxs-lookup"><span data-stu-id="87a6a-135">System.Void</span></span>

## <span data-ttu-id="87a6a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87a6a-136">NOTES</span></span>

## <span data-ttu-id="87a6a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87a6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="87a6a-138">Nowe — AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="87a6a-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="87a6a-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="87a6a-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="87a6a-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="87a6a-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


