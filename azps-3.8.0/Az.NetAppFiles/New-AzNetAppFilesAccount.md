---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 70bfdb4f590c855199bb8bbd14db4e92809b48f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894354"
---
# <span data-ttu-id="a68a6-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a68a6-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="a68a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a68a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a68a6-103">Tworzy nowe konto usługi Azure NetApp plików (ANF).</span><span class="sxs-lookup"><span data-stu-id="a68a6-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="a68a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a68a6-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a68a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a68a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a68a6-106">Polecenie cmdlet **New-AzNetAppFilesAccount** tworzy konto ANF.</span><span class="sxs-lookup"><span data-stu-id="a68a6-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="a68a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a68a6-107">EXAMPLES</span></span>

### <span data-ttu-id="a68a6-108">Przykład 1. Tworzenie konta ANF</span><span class="sxs-lookup"><span data-stu-id="a68a6-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="a68a6-109">To polecenie tworzy nowe konto ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="a68a6-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="a68a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a68a6-110">PARAMETERS</span></span>

### <span data-ttu-id="a68a6-111">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="a68a6-111">-ActiveDirectories</span></span>
<span data-ttu-id="a68a6-112">Tablica Hashtable, która reprezentuje aktywne katalogi</span><span class="sxs-lookup"><span data-stu-id="a68a6-112">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="a68a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68a6-113">-DefaultProfile</span></span>
<span data-ttu-id="a68a6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a68a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a68a6-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a68a6-115">-Location</span></span>
<span data-ttu-id="a68a6-116">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="a68a6-116">The location of the resource</span></span>

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

### <span data-ttu-id="a68a6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a68a6-117">-Name</span></span>
<span data-ttu-id="a68a6-118">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="a68a6-118">The name of the ANF account</span></span>

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

### <span data-ttu-id="a68a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a68a6-120">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="a68a6-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a68a6-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="a68a6-121">-Tag</span></span>
<span data-ttu-id="a68a6-122">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="a68a6-122">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a68a6-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a68a6-123">-Confirm</span></span>
<span data-ttu-id="a68a6-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a68a6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a68a6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a68a6-125">-WhatIf</span></span>
<span data-ttu-id="a68a6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a68a6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a68a6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a68a6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a68a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68a6-128">CommonParameters</span></span>
<span data-ttu-id="a68a6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a68a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a68a6-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68a6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68a6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a68a6-131">INPUTS</span></span>

### <span data-ttu-id="a68a6-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a68a6-132">None</span></span>

## <span data-ttu-id="a68a6-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a68a6-133">OUTPUTS</span></span>

### <span data-ttu-id="a68a6-134">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a68a6-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a68a6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a68a6-135">NOTES</span></span>

## <span data-ttu-id="a68a6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a68a6-136">RELATED LINKS</span></span>
