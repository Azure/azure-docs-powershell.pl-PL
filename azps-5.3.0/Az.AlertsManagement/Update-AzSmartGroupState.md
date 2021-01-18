---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500450"
---
# <span data-ttu-id="795c1-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="795c1-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="795c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="795c1-102">SYNOPSIS</span></span>
<span data-ttu-id="795c1-103">Stan grupy aktualizacji Smart</span><span class="sxs-lookup"><span data-stu-id="795c1-103">Updates smart group state</span></span>

## <span data-ttu-id="795c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="795c1-104">SYNTAX</span></span>

### <span data-ttu-id="795c1-105">BySmartGroupId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="795c1-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795c1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="795c1-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="795c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="795c1-107">DESCRIPTION</span></span>
<span data-ttu-id="795c1-108">Polecenie cmdlet **Update-AzSmartGroupState** umożliwia aktualizowanie stanu grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="795c1-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="795c1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="795c1-109">EXAMPLES</span></span>

### <span data-ttu-id="795c1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="795c1-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="795c1-111">To polecenie cmdlet powoduje zaktualizowanie stanu grupy inteligentnej na Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="795c1-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="795c1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="795c1-112">PARAMETERS</span></span>

### <span data-ttu-id="795c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795c1-113">-DefaultProfile</span></span>
<span data-ttu-id="795c1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="795c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795c1-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="795c1-115">-InputObject</span></span>
<span data-ttu-id="795c1-116">Obiekt wejściowy z potoku.</span><span class="sxs-lookup"><span data-stu-id="795c1-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="795c1-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="795c1-117">-SmartGroupId</span></span>
<span data-ttu-id="795c1-118">Unikatowy identyfikator grupy inteligentnej/ResourceId grupy inteligentnej.</span><span class="sxs-lookup"><span data-stu-id="795c1-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c1-119">-State</span><span class="sxs-lookup"><span data-stu-id="795c1-119">-State</span></span>
<span data-ttu-id="795c1-120">Zaktualizowany stan grupy inteligentnej</span><span class="sxs-lookup"><span data-stu-id="795c1-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="795c1-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="795c1-121">-Confirm</span></span>
<span data-ttu-id="795c1-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="795c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795c1-123">-WhatIf</span></span>
<span data-ttu-id="795c1-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="795c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795c1-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="795c1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795c1-126">CommonParameters</span></span>
<span data-ttu-id="795c1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795c1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="795c1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795c1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="795c1-129">INPUTS</span></span>

### <span data-ttu-id="795c1-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="795c1-130">None</span></span>

## <span data-ttu-id="795c1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="795c1-131">OUTPUTS</span></span>

### <span data-ttu-id="795c1-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="795c1-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="795c1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="795c1-133">NOTES</span></span>

## <span data-ttu-id="795c1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="795c1-134">RELATED LINKS</span></span>
