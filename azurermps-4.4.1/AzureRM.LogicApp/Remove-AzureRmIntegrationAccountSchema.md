---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: fc7acc34a018361b3ebaff67e57221c250e19771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718184"
---
# <span data-ttu-id="2cac4-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cac4-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="2cac4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cac4-102">SYNOPSIS</span></span>
<span data-ttu-id="2cac4-103">Umożliwia usunięcie schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2cac4-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cac4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cac4-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cac4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2cac4-105">DESCRIPTION</span></span>
<span data-ttu-id="2cac4-106">Polecenie cmdlet **Remove-AzureRmIntegrationAccountSchema** umożliwia usunięcie schematu konta integracji z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cac4-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="2cac4-107">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy schematu.</span><span class="sxs-lookup"><span data-stu-id="2cac4-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="2cac4-108">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="2cac4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2cac4-109">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="2cac4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2cac4-110">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="2cac4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2cac4-111">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="2cac4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2cac4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cac4-112">EXAMPLES</span></span>

### <span data-ttu-id="2cac4-113">Przykład 1: usuwanie schematu konta integracji</span><span class="sxs-lookup"><span data-stu-id="2cac4-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="2cac4-114">To polecenie umożliwia usunięcie schematu konta integracji o nazwie IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="2cac4-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="2cac4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cac4-115">PARAMETERS</span></span>

### <span data-ttu-id="2cac4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2cac4-116">-Force</span></span>
<span data-ttu-id="2cac4-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2cac4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2cac4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cac4-118">-Name</span></span>
<span data-ttu-id="2cac4-119">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2cac4-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="2cac4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cac4-120">-ResourceGroupName</span></span>
<span data-ttu-id="2cac4-121">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cac4-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2cac4-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2cac4-122">-SchemaName</span></span>
<span data-ttu-id="2cac4-123">Określa nazwę schematu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="2cac4-123">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="2cac4-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2cac4-124">-Confirm</span></span>
<span data-ttu-id="2cac4-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cac4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cac4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cac4-126">-WhatIf</span></span>
<span data-ttu-id="2cac4-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cac4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cac4-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2cac4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cac4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cac4-129">-DefaultProfile</span></span>
<span data-ttu-id="2cac4-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cac4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cac4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cac4-131">CommonParameters</span></span>
<span data-ttu-id="2cac4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cac4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cac4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cac4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cac4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cac4-134">INPUTS</span></span>

## <span data-ttu-id="2cac4-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cac4-135">OUTPUTS</span></span>

## <span data-ttu-id="2cac4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cac4-136">NOTES</span></span>

## <span data-ttu-id="2cac4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cac4-137">RELATED LINKS</span></span>

[<span data-ttu-id="2cac4-138">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cac4-138">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2cac4-139">Nowe — AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cac4-139">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2cac4-140">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2cac4-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


