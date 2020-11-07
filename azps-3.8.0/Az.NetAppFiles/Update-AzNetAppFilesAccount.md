---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: e6fa7a00218e52eae6b0323bc5e8ac25459986ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894181"
---
# <span data-ttu-id="74308-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="74308-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="74308-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74308-102">SYNOPSIS</span></span>
<span data-ttu-id="74308-103">Umożliwia zaktualizowanie konta usługi Azure NetApp (ANF) zgodnie z podanym opcjonalnymi modyfikatorami.</span><span class="sxs-lookup"><span data-stu-id="74308-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="74308-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74308-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="74308-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74308-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74308-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74308-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74308-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74308-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74308-108">Opis</span><span class="sxs-lookup"><span data-stu-id="74308-108">DESCRIPTION</span></span>
<span data-ttu-id="74308-109">Polecenie cmdlet **Update-AzNetAppFilesAccount** modyfikuje konto usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="74308-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="74308-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74308-110">EXAMPLES</span></span>

### <span data-ttu-id="74308-111">Przykład 1: aktualizowanie konta programu ANF</span><span class="sxs-lookup"><span data-stu-id="74308-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="74308-112">To polecenie wykonuje aktualizację na danym koncie, modyfikując odpowiednie znaczniki.</span><span class="sxs-lookup"><span data-stu-id="74308-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="74308-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74308-113">PARAMETERS</span></span>

### <span data-ttu-id="74308-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="74308-114">-ActiveDirectories</span></span>
<span data-ttu-id="74308-115">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="74308-115">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74308-116">-DefaultProfile</span></span>
<span data-ttu-id="74308-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74308-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74308-118">-InputObject</span></span>
<span data-ttu-id="74308-119">Obiekt konta do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="74308-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74308-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="74308-120">-Location</span></span>
<span data-ttu-id="74308-121">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="74308-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74308-122">-Name</span></span>
<span data-ttu-id="74308-123">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="74308-123">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74308-124">-ResourceGroupName</span></span>
<span data-ttu-id="74308-125">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="74308-125">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74308-126">-ResourceId</span></span>
<span data-ttu-id="74308-127">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="74308-127">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74308-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="74308-128">-Tag</span></span>
<span data-ttu-id="74308-129">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="74308-129">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74308-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74308-130">-Confirm</span></span>
<span data-ttu-id="74308-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74308-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74308-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74308-132">-WhatIf</span></span>
<span data-ttu-id="74308-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74308-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74308-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74308-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74308-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74308-135">CommonParameters</span></span>
<span data-ttu-id="74308-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74308-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74308-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74308-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74308-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74308-138">INPUTS</span></span>

### <span data-ttu-id="74308-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="74308-139">None</span></span>

## <span data-ttu-id="74308-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74308-140">OUTPUTS</span></span>

### <span data-ttu-id="74308-141">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="74308-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="74308-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74308-142">NOTES</span></span>

## <span data-ttu-id="74308-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74308-143">RELATED LINKS</span></span>
