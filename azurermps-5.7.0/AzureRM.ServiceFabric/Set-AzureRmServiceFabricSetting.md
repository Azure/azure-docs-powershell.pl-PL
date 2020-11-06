---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 8296945de2bcf98213fc692e486e793a91f84939
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526569"
---
# <span data-ttu-id="41541-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="41541-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="41541-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41541-102">SYNOPSIS</span></span>
<span data-ttu-id="41541-103">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="41541-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41541-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41541-104">SYNTAX</span></span>

### <span data-ttu-id="41541-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="41541-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41541-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="41541-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41541-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41541-107">DESCRIPTION</span></span>
<span data-ttu-id="41541-108">Aby dodać lub zaktualizować ustawienia sieci szkieletowej usług w klastrze, użyj **Ustawienia Set-AzureRmServiceFabricSetting** .</span><span class="sxs-lookup"><span data-stu-id="41541-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="41541-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41541-109">EXAMPLES</span></span>

### <span data-ttu-id="41541-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41541-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="41541-111">W tym poleceniu w sekcji "NamingService" zostanie ustawiona wartość "MaxFileOperationTimeout" równa "5000".</span><span class="sxs-lookup"><span data-stu-id="41541-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="41541-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41541-112">PARAMETERS</span></span>

### <span data-ttu-id="41541-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41541-113">-DefaultProfile</span></span>
<span data-ttu-id="41541-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41541-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41541-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41541-115">-Name</span></span>
<span data-ttu-id="41541-116">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="41541-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="41541-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="41541-117">-Parameter</span></span>
<span data-ttu-id="41541-118">Konstruktora.</span><span class="sxs-lookup"><span data-stu-id="41541-118">Parameter.</span></span>

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

### <span data-ttu-id="41541-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41541-119">-ResourceGroupName</span></span>
<span data-ttu-id="41541-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41541-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="41541-121">Sekcja</span><span class="sxs-lookup"><span data-stu-id="41541-121">-Section</span></span>
<span data-ttu-id="41541-122">Sekcja.</span><span class="sxs-lookup"><span data-stu-id="41541-122">Section.</span></span>

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

### <span data-ttu-id="41541-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="41541-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="41541-124">Typ uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="41541-124">Client authentication type.</span></span>

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

### <span data-ttu-id="41541-125">-Value</span><span class="sxs-lookup"><span data-stu-id="41541-125">-Value</span></span>
<span data-ttu-id="41541-126">Wartość.</span><span class="sxs-lookup"><span data-stu-id="41541-126">Value.</span></span>

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

### <span data-ttu-id="41541-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41541-127">-Confirm</span></span>
<span data-ttu-id="41541-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41541-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41541-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41541-129">-WhatIf</span></span>
<span data-ttu-id="41541-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41541-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41541-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41541-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41541-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41541-132">CommonParameters</span></span>
<span data-ttu-id="41541-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41541-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41541-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41541-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41541-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41541-135">INPUTS</span></span>

### <span data-ttu-id="41541-136">System. String</span><span class="sxs-lookup"><span data-stu-id="41541-136">System.String</span></span>
<span data-ttu-id="41541-137">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="41541-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="41541-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41541-138">OUTPUTS</span></span>

### <span data-ttu-id="41541-139">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="41541-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="41541-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41541-140">NOTES</span></span>

## <span data-ttu-id="41541-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41541-141">RELATED LINKS</span></span>

