---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894182"
---
# <span data-ttu-id="57234-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="57234-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="57234-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57234-102">SYNOPSIS</span></span>
<span data-ttu-id="57234-103">Umożliwia zaktualizowanie konta usługi Azure NetApp Files (ANF) przy użyciu nowego zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="57234-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="57234-104">Przydatne w przypadku usuwania skojarzonych z nimi aktywnych katalogów.</span><span class="sxs-lookup"><span data-stu-id="57234-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="57234-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57234-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57234-106">Opis</span><span class="sxs-lookup"><span data-stu-id="57234-106">DESCRIPTION</span></span>
<span data-ttu-id="57234-107">Polecenie cmdlet **Set-AzNetAppFilesAccount** modyfikuje konto usługi ANF.</span><span class="sxs-lookup"><span data-stu-id="57234-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="57234-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57234-108">EXAMPLES</span></span>

### <span data-ttu-id="57234-109">Przykład 1: modyfikowanie konta ANF</span><span class="sxs-lookup"><span data-stu-id="57234-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="57234-110">To polecenie wykonuje aktualizację na danym koncie.</span><span class="sxs-lookup"><span data-stu-id="57234-110">This command performs an update on the given account.</span></span> <span data-ttu-id="57234-111">Brak usługi Active Directory oznacza, że zostanie ona usunięta z konta.</span><span class="sxs-lookup"><span data-stu-id="57234-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="57234-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57234-112">PARAMETERS</span></span>

### <span data-ttu-id="57234-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="57234-113">-ActiveDirectories</span></span>
<span data-ttu-id="57234-114">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="57234-114">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="57234-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57234-115">-DefaultProfile</span></span>
<span data-ttu-id="57234-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="57234-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57234-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="57234-117">-Location</span></span>
<span data-ttu-id="57234-118">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="57234-118">The location of the resource</span></span>

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

### <span data-ttu-id="57234-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="57234-119">-Name</span></span>
<span data-ttu-id="57234-120">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="57234-120">The name of the ANF account</span></span>

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

### <span data-ttu-id="57234-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57234-121">-ResourceGroupName</span></span>
<span data-ttu-id="57234-122">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="57234-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="57234-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="57234-123">-Tag</span></span>
<span data-ttu-id="57234-124">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="57234-124">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="57234-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57234-125">-Confirm</span></span>
<span data-ttu-id="57234-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57234-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57234-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57234-127">-WhatIf</span></span>
<span data-ttu-id="57234-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57234-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57234-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="57234-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57234-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57234-130">CommonParameters</span></span>
<span data-ttu-id="57234-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57234-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="57234-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57234-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57234-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57234-133">INPUTS</span></span>

### <span data-ttu-id="57234-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="57234-134">None</span></span>

## <span data-ttu-id="57234-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57234-135">OUTPUTS</span></span>

### <span data-ttu-id="57234-136">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="57234-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="57234-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57234-137">NOTES</span></span>

## <span data-ttu-id="57234-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57234-138">RELATED LINKS</span></span>
