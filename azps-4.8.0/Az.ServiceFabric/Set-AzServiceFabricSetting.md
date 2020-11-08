---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 72a538c039914eebdcd2926cda93a97cfe2d267a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221106"
---
# <span data-ttu-id="ad2d6-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ad2d6-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="ad2d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2d6-103">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="ad2d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad2d6-104">SYNTAX</span></span>

### <span data-ttu-id="ad2d6-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="ad2d6-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad2d6-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="ad2d6-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2d6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad2d6-107">DESCRIPTION</span></span>
<span data-ttu-id="ad2d6-108">Aby dodać lub zaktualizować ustawienia sieci szkieletowej usług w klastrze, użyj **Ustawienia Set-AzServiceFabricSetting** .</span><span class="sxs-lookup"><span data-stu-id="ad2d6-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="ad2d6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad2d6-109">EXAMPLES</span></span>

### <span data-ttu-id="ad2d6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad2d6-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="ad2d6-111">W tym poleceniu w sekcji "NamingService" zostanie ustawiona wartość "MaxFileOperationTimeout" równa "5000".</span><span class="sxs-lookup"><span data-stu-id="ad2d6-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="ad2d6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad2d6-112">PARAMETERS</span></span>

### <span data-ttu-id="ad2d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2d6-113">-DefaultProfile</span></span>
<span data-ttu-id="ad2d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad2d6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad2d6-115">-Name</span></span>
<span data-ttu-id="ad2d6-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="ad2d6-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ad2d6-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="ad2d6-117">-Parameter</span></span>
<span data-ttu-id="ad2d6-118">Nazwa parametru ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="ad2d6-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="ad2d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad2d6-120">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ad2d6-121">Sekcja</span><span class="sxs-lookup"><span data-stu-id="ad2d6-121">-Section</span></span>
<span data-ttu-id="ad2d6-122">Nazwa sekcji Ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="ad2d6-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="ad2d6-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="ad2d6-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="ad2d6-124">Tablica ustawień sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="ad2d6-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="ad2d6-125">-Value</span><span class="sxs-lookup"><span data-stu-id="ad2d6-125">-Value</span></span>
<span data-ttu-id="ad2d6-126">Wartość parametru ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="ad2d6-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="ad2d6-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad2d6-127">-Confirm</span></span>
<span data-ttu-id="ad2d6-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2d6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2d6-129">-WhatIf</span></span>
<span data-ttu-id="ad2d6-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2d6-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2d6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2d6-132">CommonParameters</span></span>
<span data-ttu-id="ad2d6-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad2d6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2d6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad2d6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2d6-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad2d6-135">INPUTS</span></span>

### <span data-ttu-id="ad2d6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ad2d6-136">System.String</span></span>

### <span data-ttu-id="ad2d6-137">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="ad2d6-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="ad2d6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad2d6-138">OUTPUTS</span></span>

### <span data-ttu-id="ad2d6-139">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ad2d6-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ad2d6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad2d6-140">NOTES</span></span>

## <span data-ttu-id="ad2d6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad2d6-141">RELATED LINKS</span></span>
