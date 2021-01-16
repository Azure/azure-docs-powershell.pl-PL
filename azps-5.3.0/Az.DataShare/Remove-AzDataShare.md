---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377204"
---
# <span data-ttu-id="35127-101">Remove-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="35127-101">Remove-AzDataShare</span></span>

## <span data-ttu-id="35127-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="35127-102">SYNOPSIS</span></span>
<span data-ttu-id="35127-103">Umożliwia usunięcie udziału danych.</span><span class="sxs-lookup"><span data-stu-id="35127-103">Removes a data share.</span></span>

## <span data-ttu-id="35127-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="35127-104">SYNTAX</span></span>

### <span data-ttu-id="35127-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="35127-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35127-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35127-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35127-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35127-108">Opis</span><span class="sxs-lookup"><span data-stu-id="35127-108">DESCRIPTION</span></span>
<span data-ttu-id="35127-109">Polecenie cmdlet **Remove-AzDataShare** umożliwia usunięcie udziału danych.</span><span class="sxs-lookup"><span data-stu-id="35127-109">The **Remove-AzDataShare** cmdlet removes a data share.</span></span>

## <span data-ttu-id="35127-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="35127-110">EXAMPLES</span></span>

### <span data-ttu-id="35127-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="35127-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="35127-112">To polecenie usuwa udział danych o nazwie AdsShare z konta usługi Azure Data Share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="35127-112">This commands removes the data share named AdsShare from the azure data share account WikiAds.</span></span> 

## <span data-ttu-id="35127-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="35127-113">PARAMETERS</span></span>

### <span data-ttu-id="35127-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="35127-114">-AccountName</span></span>
<span data-ttu-id="35127-115">Nazwa konta udziału danych w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="35127-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35127-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35127-116">-AsJob</span></span>
<span data-ttu-id="35127-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="35127-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="35127-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35127-118">-DefaultProfile</span></span>
<span data-ttu-id="35127-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="35127-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35127-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35127-120">-InputObject</span></span>
<span data-ttu-id="35127-121">Obiekt udziału danych platformy Azure "' YAML typ: PSDataShare zestawy parametrów: aliasy ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="35127-121">Azure data share object\` \`\`yaml Type: PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span> 

<span data-ttu-id="35127-122">Wymagane: prawda położenia: nazwana wartość domyślna: brak Akceptuj dane wejściowe potoku: prawda (ByValue) akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-122">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35127-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="35127-123">-Name</span></span>
<span data-ttu-id="35127-124">Nazwa udziału danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="35127-124">Azure data share name</span></span>

<span data-ttu-id="35127-125">YAML, typ: zestawy parametrów ciągów: ByFieldsParameterSet aliasy:</span><span class="sxs-lookup"><span data-stu-id="35127-125">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="35127-126">Wymagane: prawda położenia: nazwana wartość domyślna: brak akceptowania danych wejściowych potoku: FAŁSZ akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-126">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35127-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35127-127">-PassThru</span></span>
<span data-ttu-id="35127-128">Zwraca obiekt (jeśli jest określony).</span><span class="sxs-lookup"><span data-stu-id="35127-128">Return object (if specified).</span></span>

<span data-ttu-id="35127-129">Typ YAML: SwitchParameter zestawy parametrów: (wszystkie) aliasy:</span><span class="sxs-lookup"><span data-stu-id="35127-129">yaml Type: SwitchParameter Parameter Sets: (All) Aliases:</span></span> 

<span data-ttu-id="35127-130">Wymagane: fałszowanie pozycji: nazwana wartość domyślna: brak akceptowania danych wejściowych potoku: FAŁSZ akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-130">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="35127-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35127-131">-ResourceGroupName</span></span>
<span data-ttu-id="35127-132">Nazwa grupy zasobów konta usługi Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="35127-132">The resource group name of the azure data share account</span></span>

<span data-ttu-id="35127-133">YAML, typ: zestawy parametrów ciągów: ByFieldsParameterSet aliasy:</span><span class="sxs-lookup"><span data-stu-id="35127-133">yaml Type: String Parameter Sets: ByFieldsParameterSet Aliases:</span></span> 

<span data-ttu-id="35127-134">Wymagane: prawda położenia: nazwana wartość domyślna: brak akceptowania danych wejściowych potoku: FAŁSZ akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-134">Required: True Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35127-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35127-135">-ResourceId</span></span>
<span data-ttu-id="35127-136">Identyfikator zasobu udziału danych usługi Azure</span><span class="sxs-lookup"><span data-stu-id="35127-136">The resource id of the Azure data share</span></span>

<span data-ttu-id="35127-137">YAML, typ: zestawy parametrów ciągów: ByResourceIdParameterSet aliasy:</span><span class="sxs-lookup"><span data-stu-id="35127-137">yaml Type: String Parameter Sets: ByResourceIdParameterSet Aliases:</span></span> 

<span data-ttu-id="35127-138">Wymagane: prawda położenia: nazwana wartość domyślna: brak Akceptuj dane wejściowe potoku: prawda (ByPropertyName) akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-138">Required: True Position: Named Default value: None Accept pipeline input: True (ByPropertyName) Accept wildcard characters: False</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35127-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="35127-139">-Confirm</span></span>
<span data-ttu-id="35127-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35127-140">Prompts you for confirmation before running the cmdlet.</span></span>

<span data-ttu-id="35127-141">YAML, typ: SwitchParameter zestawy parametrów: (wszystkie) aliasy: CF</span><span class="sxs-lookup"><span data-stu-id="35127-141">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: cf</span></span>

<span data-ttu-id="35127-142">Wymagane: fałszowanie pozycji: nazwana wartość domyślna: brak akceptowania danych wejściowych potoku: FAŁSZ akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-142">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="35127-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35127-143">-WhatIf</span></span>
<span data-ttu-id="35127-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35127-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35127-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="35127-145">The cmdlet is not run.</span></span>

<span data-ttu-id="35127-146">YAML, typ: SwitchParameter zestawy parametrów: (wszystkie) aliasy: Wi</span><span class="sxs-lookup"><span data-stu-id="35127-146">yaml Type: SwitchParameter Parameter Sets: (All) Aliases: wi</span></span>

<span data-ttu-id="35127-147">Wymagane: fałszowanie pozycji: nazwana wartość domyślna: brak akceptowania danych wejściowych potoku: FAŁSZ akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-147">Required: False Position: Named Default value: None Accept pipeline input: False Accept wildcard characters: False</span></span>




<span data-ttu-id="35127-148">Typ YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare zestawów parametrów: aliasy ByObjectParameterSet:</span><span class="sxs-lookup"><span data-stu-id="35127-148">yaml Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare Parameter Sets: ByObjectParameterSet Aliases:</span></span>

<span data-ttu-id="35127-149">Wymagane: prawda położenia: nazwana wartość domyślna: brak Akceptuj dane wejściowe potoku: prawda (ByValue) akceptowanie symboli wieloznacznych: FAŁSZ</span><span class="sxs-lookup"><span data-stu-id="35127-149">Required: True Position: Named Default value: None Accept pipeline input: True (ByValue) Accept wildcard characters: False</span></span>

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

### <span data-ttu-id="35127-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35127-150">CommonParameters</span></span>
<span data-ttu-id="35127-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35127-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35127-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35127-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35127-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="35127-153">INPUTS</span></span>

### <span data-ttu-id="35127-154">System. String</span><span class="sxs-lookup"><span data-stu-id="35127-154">System.String</span></span>

### <span data-ttu-id="35127-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="35127-155">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="35127-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="35127-156">OUTPUTS</span></span>

### <span data-ttu-id="35127-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35127-157">System.Boolean</span></span>

## <span data-ttu-id="35127-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="35127-158">NOTES</span></span>

## <span data-ttu-id="35127-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="35127-159">RELATED LINKS</span></span>
