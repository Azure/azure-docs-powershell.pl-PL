---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 5d5c5092580c8e86966bb15aaf538702c42483a6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892058"
---
# <span data-ttu-id="34239-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="34239-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="34239-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34239-102">SYNOPSIS</span></span>
<span data-ttu-id="34239-103">Usuwa tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="34239-103">Removes a storage table.</span></span>

## <span data-ttu-id="34239-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34239-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34239-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34239-105">DESCRIPTION</span></span>
<span data-ttu-id="34239-106">Polecenie cmdlet **Remove-AzStorageTable** usuwa co najmniej jeden magazyn z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="34239-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="34239-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34239-107">EXAMPLES</span></span>

### <span data-ttu-id="34239-108">Przykład 1. Usuwanie tabeli</span><span class="sxs-lookup"><span data-stu-id="34239-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="34239-109">To polecenie umożliwia usunięcie tabeli.</span><span class="sxs-lookup"><span data-stu-id="34239-109">This command removes a table.</span></span>

### <span data-ttu-id="34239-110">Przykład 2: Usuwanie kilku tabel</span><span class="sxs-lookup"><span data-stu-id="34239-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="34239-111">W tym przykładzie użyto symbolu wieloznacznego z parametrem *name* w celu uzyskania wszystkich tabel pasujących do tabeli wzorzec, a następnie przekazanie wyniku w potoku w celu usunięcia tabel.</span><span class="sxs-lookup"><span data-stu-id="34239-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="34239-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34239-112">PARAMETERS</span></span>

### <span data-ttu-id="34239-113">-Context</span><span class="sxs-lookup"><span data-stu-id="34239-113">-Context</span></span>
<span data-ttu-id="34239-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="34239-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="34239-115">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="34239-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34239-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34239-116">-DefaultProfile</span></span>
<span data-ttu-id="34239-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34239-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34239-118">-Force</span><span class="sxs-lookup"><span data-stu-id="34239-118">-Force</span></span>
<span data-ttu-id="34239-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="34239-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34239-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34239-120">-Name</span></span>
<span data-ttu-id="34239-121">Określa nazwę tabeli, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="34239-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34239-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34239-122">-PassThru</span></span>
<span data-ttu-id="34239-123">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="34239-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="34239-124">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="34239-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="34239-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34239-125">-Confirm</span></span>
<span data-ttu-id="34239-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34239-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34239-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34239-127">-WhatIf</span></span>
<span data-ttu-id="34239-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34239-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34239-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34239-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34239-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34239-130">CommonParameters</span></span>
<span data-ttu-id="34239-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34239-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34239-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34239-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34239-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34239-133">INPUTS</span></span>

### <span data-ttu-id="34239-134">System. String</span><span class="sxs-lookup"><span data-stu-id="34239-134">System.String</span></span>

### <span data-ttu-id="34239-135">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34239-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34239-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34239-136">OUTPUTS</span></span>

### <span data-ttu-id="34239-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34239-137">System.Boolean</span></span>

## <span data-ttu-id="34239-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34239-138">NOTES</span></span>

## <span data-ttu-id="34239-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34239-139">RELATED LINKS</span></span>

[<span data-ttu-id="34239-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="34239-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
