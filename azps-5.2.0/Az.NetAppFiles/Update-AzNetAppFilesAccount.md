---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351490"
---
# <span data-ttu-id="bafec-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bafec-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="bafec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bafec-102">SYNOPSIS</span></span>
<span data-ttu-id="bafec-103">Umożliwia zaktualizowanie konta usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="bafec-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="bafec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bafec-104">SYNTAX</span></span>

### <span data-ttu-id="bafec-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bafec-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafec-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bafec-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bafec-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bafec-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bafec-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bafec-108">DESCRIPTION</span></span>
<span data-ttu-id="bafec-109">Polecenie cmdlet **Update-AzNetAppFilesAccount** modyfikuje konto usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="bafec-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="bafec-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bafec-110">EXAMPLES</span></span>

### <span data-ttu-id="bafec-111">Przykład 1: aktualizowanie konta programu ANF</span><span class="sxs-lookup"><span data-stu-id="bafec-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="bafec-112">To polecenie wykonuje aktualizację na danym koncie, modyfikując odpowiednie znaczniki.</span><span class="sxs-lookup"><span data-stu-id="bafec-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="bafec-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bafec-113">PARAMETERS</span></span>

### <span data-ttu-id="bafec-114">-Pozycji</span><span class="sxs-lookup"><span data-stu-id="bafec-114">-ActiveDirectory</span></span>
<span data-ttu-id="bafec-115">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="bafec-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafec-116">-DefaultProfile</span></span>
<span data-ttu-id="bafec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bafec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bafec-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bafec-118">-InputObject</span></span>
<span data-ttu-id="bafec-119">Obiekt konta do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="bafec-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bafec-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bafec-120">-Location</span></span>
<span data-ttu-id="bafec-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="bafec-121">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafec-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bafec-122">-Name</span></span>
<span data-ttu-id="bafec-123">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="bafec-123">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafec-124">-ResourceGroupName</span></span>
<span data-ttu-id="bafec-125">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="bafec-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="bafec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bafec-126">-ResourceId</span></span>
<span data-ttu-id="bafec-127">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="bafec-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="bafec-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="bafec-128">-Tag</span></span>
<span data-ttu-id="bafec-129">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="bafec-129">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafec-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bafec-130">-Confirm</span></span>
<span data-ttu-id="bafec-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bafec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafec-132">-WhatIf</span></span>
<span data-ttu-id="bafec-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafec-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bafec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bafec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafec-135">CommonParameters</span></span>
<span data-ttu-id="bafec-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafec-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bafec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafec-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bafec-138">INPUTS</span></span>

### <span data-ttu-id="bafec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bafec-139">System.String</span></span>

### <span data-ttu-id="bafec-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bafec-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bafec-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bafec-141">OUTPUTS</span></span>

### <span data-ttu-id="bafec-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bafec-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bafec-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bafec-143">NOTES</span></span>

## <span data-ttu-id="bafec-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bafec-144">RELATED LINKS</span></span>
