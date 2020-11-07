---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718585"
---
# <span data-ttu-id="86381-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="86381-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="86381-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86381-102">SYNOPSIS</span></span>
<span data-ttu-id="86381-103">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="86381-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86381-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86381-104">SYNTAX</span></span>

### <span data-ttu-id="86381-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="86381-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86381-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="86381-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86381-107">Opis</span><span class="sxs-lookup"><span data-stu-id="86381-107">DESCRIPTION</span></span>
<span data-ttu-id="86381-108">Użyj narzędzia **Remove-AzureRmServiceFabricSetting** , aby usunąć ustawienia sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="86381-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="86381-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86381-109">EXAMPLES</span></span>

### <span data-ttu-id="86381-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86381-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="86381-111">To polecenie usunie ustawienia "MaxCursors" w sekcji "EseStore".</span><span class="sxs-lookup"><span data-stu-id="86381-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="86381-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86381-112">PARAMETERS</span></span>

### <span data-ttu-id="86381-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86381-113">-DefaultProfile</span></span>
<span data-ttu-id="86381-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86381-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86381-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86381-115">-Name</span></span>
<span data-ttu-id="86381-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="86381-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86381-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="86381-117">-Parameter</span></span>
<span data-ttu-id="86381-118">Konstruktora.</span><span class="sxs-lookup"><span data-stu-id="86381-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86381-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86381-119">-ResourceGroupName</span></span>
<span data-ttu-id="86381-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86381-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="86381-121">Sekcja</span><span class="sxs-lookup"><span data-stu-id="86381-121">-Section</span></span>
<span data-ttu-id="86381-122">Sekcja.</span><span class="sxs-lookup"><span data-stu-id="86381-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86381-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="86381-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="86381-124">Typ uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="86381-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86381-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86381-125">-Confirm</span></span>
<span data-ttu-id="86381-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86381-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86381-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86381-127">-WhatIf</span></span>
<span data-ttu-id="86381-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86381-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86381-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86381-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86381-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86381-130">CommonParameters</span></span>
<span data-ttu-id="86381-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86381-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86381-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86381-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86381-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86381-133">INPUTS</span></span>

### <span data-ttu-id="86381-134">System. String</span><span class="sxs-lookup"><span data-stu-id="86381-134">System.String</span></span>
<span data-ttu-id="86381-135">Parametry: Parameter (ByValue), sekcja (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86381-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="86381-136">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="86381-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="86381-137">Parametry: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86381-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="86381-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86381-138">OUTPUTS</span></span>

### <span data-ttu-id="86381-139">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="86381-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="86381-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86381-140">NOTES</span></span>

## <span data-ttu-id="86381-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86381-141">RELATED LINKS</span></span>
