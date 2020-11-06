---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550012"
---
# <span data-ttu-id="7f45b-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7f45b-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="7f45b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7f45b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f45b-103">Trwale usuwa konto Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f45b-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f45b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7f45b-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f45b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7f45b-105">DESCRIPTION</span></span>
<span data-ttu-id="7f45b-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreAccount** umożliwia trwałe usunięcie konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f45b-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="7f45b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7f45b-107">EXAMPLES</span></span>

### <span data-ttu-id="7f45b-108">Przykład 1. Usuń konto w usłudze Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7f45b-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="7f45b-109">To polecenie usuwa konto o nazwie ContosoADL z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f45b-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="7f45b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7f45b-110">PARAMETERS</span></span>

### <span data-ttu-id="7f45b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7f45b-111">-Force</span></span>
<span data-ttu-id="7f45b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7f45b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f45b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7f45b-113">-Name</span></span>
<span data-ttu-id="7f45b-114">Określa nazwę konta, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="7f45b-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="7f45b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f45b-115">-PassThru</span></span>
<span data-ttu-id="7f45b-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7f45b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f45b-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7f45b-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f45b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f45b-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f45b-119">Określa grupę zasobów zawierającą konto do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="7f45b-119">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f45b-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f45b-120">-Confirm</span></span>
<span data-ttu-id="7f45b-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f45b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f45b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f45b-122">-WhatIf</span></span>
<span data-ttu-id="7f45b-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f45b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f45b-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7f45b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f45b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f45b-125">-DefaultProfile</span></span>
<span data-ttu-id="7f45b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f45b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f45b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f45b-127">CommonParameters</span></span>
<span data-ttu-id="7f45b-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f45b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f45b-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f45b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f45b-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f45b-130">INPUTS</span></span>

## <span data-ttu-id="7f45b-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7f45b-131">OUTPUTS</span></span>

### <span data-ttu-id="7f45b-132">logiczną</span><span class="sxs-lookup"><span data-stu-id="7f45b-132">bool</span></span>
<span data-ttu-id="7f45b-133">Jeśli PassThru jest określony, zwraca wartość Prawda po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="7f45b-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="7f45b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7f45b-134">NOTES</span></span>

## <span data-ttu-id="7f45b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f45b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7f45b-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7f45b-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7f45b-137">Nowe — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7f45b-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7f45b-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7f45b-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="7f45b-139">Test — AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="7f45b-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


