---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 1137ba802bc1ccd920b45c895b70aee2f8a8e7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867631"
---
# <span data-ttu-id="4cee2-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4cee2-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="4cee2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cee2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cee2-103">Umożliwia usunięcie schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4cee2-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="4cee2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cee2-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cee2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4cee2-105">DESCRIPTION</span></span>
<span data-ttu-id="4cee2-106">Polecenie cmdlet **Remove-AzIntegrationAccountSchema** umożliwia usunięcie schematu konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cee2-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="4cee2-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="4cee2-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="4cee2-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="4cee2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4cee2-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="4cee2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4cee2-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="4cee2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4cee2-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="4cee2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4cee2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cee2-112">EXAMPLES</span></span>

### <span data-ttu-id="4cee2-113">Przykład 1: usuwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="4cee2-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="4cee2-114">To polecenie umożliwia usunięcie schematu konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="4cee2-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="4cee2-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cee2-115">PARAMETERS</span></span>

### <span data-ttu-id="4cee2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cee2-116">-DefaultProfile</span></span>
<span data-ttu-id="4cee2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4cee2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cee2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4cee2-118">-Force</span></span>
<span data-ttu-id="4cee2-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4cee2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cee2-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4cee2-120">-Name</span></span>
<span data-ttu-id="4cee2-121">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4cee2-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="4cee2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cee2-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cee2-123">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cee2-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4cee2-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4cee2-124">-SchemaName</span></span>
<span data-ttu-id="4cee2-125">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="4cee2-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="4cee2-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cee2-126">-Confirm</span></span>
<span data-ttu-id="4cee2-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cee2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cee2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cee2-128">-WhatIf</span></span>
<span data-ttu-id="4cee2-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cee2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cee2-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cee2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cee2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cee2-131">CommonParameters</span></span>
<span data-ttu-id="4cee2-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cee2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cee2-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cee2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cee2-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cee2-134">INPUTS</span></span>

### <span data-ttu-id="4cee2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4cee2-135">System.String</span></span>

## <span data-ttu-id="4cee2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cee2-136">OUTPUTS</span></span>

### <span data-ttu-id="4cee2-137">System. void</span><span class="sxs-lookup"><span data-stu-id="4cee2-137">System.Void</span></span>

## <span data-ttu-id="4cee2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cee2-138">NOTES</span></span>

## <span data-ttu-id="4cee2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cee2-139">RELATED LINKS</span></span>

[<span data-ttu-id="4cee2-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4cee2-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="4cee2-141">Nowe — AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4cee2-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="4cee2-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="4cee2-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


