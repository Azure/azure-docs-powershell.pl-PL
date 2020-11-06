---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 47e1e33f282cbb238c6bbb53bb007d593b9c043f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526573"
---
# <span data-ttu-id="9472f-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="9472f-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="9472f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9472f-102">SYNOPSIS</span></span>
<span data-ttu-id="9472f-103">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="9472f-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9472f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9472f-104">SYNTAX</span></span>

### <span data-ttu-id="9472f-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="9472f-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9472f-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="9472f-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9472f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9472f-107">DESCRIPTION</span></span>
<span data-ttu-id="9472f-108">Użyj narzędzia **Remove-AzureRmServiceFabricSetting** , aby usunąć ustawienia sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="9472f-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="9472f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9472f-109">EXAMPLES</span></span>

### <span data-ttu-id="9472f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9472f-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="9472f-111">To polecenie usunie ustawienia "MaxCursors" w sekcji "EseStore".</span><span class="sxs-lookup"><span data-stu-id="9472f-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="9472f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9472f-112">PARAMETERS</span></span>

### <span data-ttu-id="9472f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9472f-113">-DefaultProfile</span></span>
<span data-ttu-id="9472f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9472f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9472f-115">-Name</span></span>
<span data-ttu-id="9472f-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="9472f-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9472f-117">-Parameter</span></span>
<span data-ttu-id="9472f-118">Konstruktora.</span><span class="sxs-lookup"><span data-stu-id="9472f-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9472f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9472f-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9472f-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-121">Sekcja</span><span class="sxs-lookup"><span data-stu-id="9472f-121">-Section</span></span>
<span data-ttu-id="9472f-122">Sekcja.</span><span class="sxs-lookup"><span data-stu-id="9472f-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="9472f-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="9472f-124">Typ uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="9472f-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9472f-125">-Confirm</span></span>
<span data-ttu-id="9472f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9472f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9472f-127">-WhatIf</span></span>
<span data-ttu-id="9472f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9472f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9472f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9472f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9472f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9472f-130">CommonParameters</span></span>
<span data-ttu-id="9472f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9472f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9472f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9472f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9472f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9472f-133">INPUTS</span></span>

### <span data-ttu-id="9472f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9472f-134">System.String</span></span>
<span data-ttu-id="9472f-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="9472f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="9472f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9472f-136">OUTPUTS</span></span>

### <span data-ttu-id="9472f-137">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="9472f-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="9472f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9472f-138">NOTES</span></span>

## <span data-ttu-id="9472f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9472f-139">RELATED LINKS</span></span>

