---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356221"
---
# <span data-ttu-id="bbf83-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="bbf83-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="bbf83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bbf83-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf83-103">Modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bbf83-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bbf83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bbf83-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf83-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bbf83-105">DESCRIPTION</span></span>
<span data-ttu-id="bbf83-106">Polecenie cmdlet **Set-AzDataLakeStoreItemOwner** modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bbf83-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bbf83-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bbf83-107">EXAMPLES</span></span>

### <span data-ttu-id="bbf83-108">Przykład 1. Ustawianie właściciela elementu</span><span class="sxs-lookup"><span data-stu-id="bbf83-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="bbf83-109">To polecenie ustawia właściciela katalogu głównego, aby Patti pełen.</span><span class="sxs-lookup"><span data-stu-id="bbf83-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="bbf83-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bbf83-110">PARAMETERS</span></span>

### <span data-ttu-id="bbf83-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="bbf83-111">-Account</span></span>
<span data-ttu-id="bbf83-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bbf83-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf83-113">-DefaultProfile</span></span>
<span data-ttu-id="bbf83-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bbf83-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbf83-115">-ID</span><span class="sxs-lookup"><span data-stu-id="bbf83-115">-Id</span></span>
<span data-ttu-id="bbf83-116">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive, który ma być używany jako właściciel.</span><span class="sxs-lookup"><span data-stu-id="bbf83-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf83-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf83-117">-PassThru</span></span>
<span data-ttu-id="bbf83-118">Wskazuje, że zaktualizowany właściciel powinien zostać zwrócony.</span><span class="sxs-lookup"><span data-stu-id="bbf83-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf83-119">-Path</span><span class="sxs-lookup"><span data-stu-id="bbf83-119">-Path</span></span>
<span data-ttu-id="bbf83-120">Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="bbf83-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf83-121">-Type</span><span class="sxs-lookup"><span data-stu-id="bbf83-121">-Type</span></span>
<span data-ttu-id="bbf83-122">Określa typ właściciela do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="bbf83-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="bbf83-123">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="bbf83-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbf83-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bbf83-124">-Confirm</span></span>
<span data-ttu-id="bbf83-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf83-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf83-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf83-126">-WhatIf</span></span>
<span data-ttu-id="bbf83-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbf83-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf83-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bbf83-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf83-129">CommonParameters</span></span>
<span data-ttu-id="bbf83-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbf83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf83-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf83-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf83-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bbf83-132">INPUTS</span></span>

### <span data-ttu-id="bbf83-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf83-133">System.String</span></span>

### <span data-ttu-id="bbf83-134">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bbf83-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bbf83-135">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="bbf83-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="bbf83-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bbf83-136">System.Guid</span></span>

### <span data-ttu-id="bbf83-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bbf83-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bbf83-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bbf83-138">OUTPUTS</span></span>

### <span data-ttu-id="bbf83-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bbf83-139">System.String</span></span>

## <span data-ttu-id="bbf83-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bbf83-140">NOTES</span></span>

## <span data-ttu-id="bbf83-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bbf83-141">RELATED LINKS</span></span>

[<span data-ttu-id="bbf83-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="bbf83-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


